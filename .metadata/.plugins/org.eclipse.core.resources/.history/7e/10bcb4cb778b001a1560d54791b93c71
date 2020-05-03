package com.cts.service;

import java.util.List;
import java.util.Optional;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import com.cts.entity.Vendor;
import com.cts.repository.VendorRepository;

@Service
public class VendorService {
	@Autowired
	VendorRepository repo;
	
	public void addVendor(Vendor vendor) {
		repo.save(vendor);
		
	}
	public List<Vendor> getAllVendor() {
		// TODO Auto-generated method stub
		return (List<Vendor>) repo.findAll();
	}

	public Optional<Vendor> getVendorById(long vendorId) {
		
		return repo.findById(vendorId);
	}
	public void deleteVendor(Long vendorId) {
		repo.deleteById(vendorId);
	}
	public void updateVendor(Vendor vendor,long vendorId) {
		repo.save(vendor);
		
	}

}

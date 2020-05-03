package com.cts.controller;

import java.util.List;
import java.util.Optional;
import javax.validation.Valid;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestMethod;
import org.springframework.web.bind.annotation.RestController;

import com.cts.entity.Vendor;
import com.cts.service.VendorService;

@RestController
@CrossOrigin
public class VendorController {
	@Autowired
	VendorService service;
	@RequestMapping("/vendors")
	List<Vendor> getAllVendors() {
		return service.getAllVendor();
	}

	@RequestMapping(method=RequestMethod.POST,value="/addvendor")
	void addVendor(@Valid @RequestBody Vendor vendor) {
		service.addVendor(vendor);
	}
	
	@RequestMapping(method = RequestMethod.DELETE, value="/{vendorid}")
	void deleteVendorById(@PathVariable Long vendorId) {
		service.deleteVendor(vendorId);
	}
	@RequestMapping(method=RequestMethod.PUT,value="/upvendor/{vendorId}")
	void updateVendor(@Valid @RequestBody Vendor vendor, @PathVariable long vendorId) {
		service.updateVendor(vendor,vendorId);
	}
	
	@RequestMapping("/{vendorId}")
	Optional<Vendor> getVendorById(@PathVariable long vendorId) {
		return service.getVendorById(vendorId);
	}


}

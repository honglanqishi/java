package com.test.controller;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.ResponseBody;

import com.alibaba.fastjson.JSON;
import com.alibaba.fastjson.JSONArray;
import com.test.dao.userDao;
import com.test.vo.user;

@Controller
@RequestMapping("test")
public class TestController {
	
	
	@Autowired
	private userDao userdao;
	
	@RequestMapping("test1")
	@ResponseBody
	public Object test1(){
		
		user u=userdao.findUser();
		System.out.println(u.getUserId()+","+u.getUserName());
		JSON j = (JSON) JSONArray.toJSON(u);
		return "Test1:"+System.currentTimeMillis()+"============="+j;
	}
}

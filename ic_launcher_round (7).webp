package com.example.mobappprog_2

import android.os.Bundle
import android.widget.TextView
import android.widget.Toast
import androidx.activity.enableEdgeToEdge
import androidx.appcompat.app.AppCompatActivity
import androidx.core.view.ViewCompat
import androidx.core.view.WindowInsetsCompat
import com.google.android.gms.maps.CameraUpdate
import com.google.android.gms.maps.CameraUpdateFactory
import com.google.android.gms.maps.GoogleMap
import com.google.android.gms.maps.OnMapReadyCallback
import com.google.android.gms.maps.SupportMapFragment
import com.google.android.gms.maps.model.LatLng
import com.google.android.gms.maps.model.Marker
import com.google.android.gms.maps.model.MarkerOptions

class MainActivity : AppCompatActivity(), OnMapReadyCallback {

    lateinit var mMap:GoogleMap

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_main)
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->
            val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)
            insets
        }

        var mapFragment = supportFragmentManager.findFragmentById(R.id.map) as SupportMapFragment
        mapFragment.getMapAsync(this)
    }

    override fun onMapReady(googleMap: GoogleMap) {
        mMap = googleMap
        var point1 = LatLng(54.724406, 55.940660)
        var point2 = LatLng(54.724862, 55.941333)
        var point3 = LatLng(54.725901, 55.943818)
        var point4 = LatLng(54.724716, 55.941813)
        var point5 = LatLng(54.725868, 55.946412)
        var point6 = LatLng(54.725577, 55.942063)
        var point7 = LatLng(54.725018, 55.942222)

        mMap.addMarker(MarkerOptions().position(point1)
            .title("Аудитория 6-419")
            .snippet("Аудитория, в которой сдаетя данная лабораторная работа"))
        mMap.addMarker(MarkerOptions().position(point2)
            .title("Вход 6 корпуса")
            .snippet("Широкий вход с закрытыми дверьми"))
        mMap.addMarker(MarkerOptions().position(point3)
            .title("Вход 9 корпуса")
            .snippet("Узкий вход с открытыми дверьми"))
        mMap.addMarker(MarkerOptions().position(point4)
            .title("Самолет")
            .snippet("Находится в самом центре территории ВУЗа"))
        mMap.addMarker(MarkerOptions().position(point5)
            .title("Владимир Ленин")
            .snippet("Имеет самый большой размер обуви в Уфе"))
        mMap.addMarker(MarkerOptions().position(point6)
            .title("Автобус")
            .snippet("Предназначен для перевозки людей"))
        mMap.addMarker(MarkerOptions().position(point7)
            .title("Часы")
            .snippet("Показывают время, давление и температуру"))

        mMap.isBuildingsEnabled = true
        mMap.isIndoorEnabled = true

        mMap.moveCamera(CameraUpdateFactory.newLatLng(point1))
    }
}

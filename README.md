start kotlin with redux
library: ReKotlin

Learning source: https://android.jlelse.eu/redux-rxkotlin-rxswift-awesome-native-mobile-apps-series-ebc7882162f8

App State: (have many sub states)
	Là một khái niệm kiểu model (ví dụ như user, userProfile, offer,...)
	
	State is read-only:
		-Không phải mọi functions  trong ứng dụng đều có thể cập nhật trạng thái, thay vào đó, có một cơ chế nhất quán để cập nhật trạng thái.
		-Thậm chí ngay cả một callback từ network cũng không được phép tac động vào state.
	Pure functions change state: (Reducer)
		-reducers sẽ không trực tiếp thay đổi state mà nó nhận được, mà tạo ra các bản copy và thay đổi trên đó. 
		-> Sau khi state thay đổi: các component (Fragments and Activities components in Android, viewcontroller, and Views are components in iOS.) sẽ thay đổi theo state.
			Cơ chế: các components sẽ subscrible state. Sau khi state updated, sẽ tạo ra event để update lại components.


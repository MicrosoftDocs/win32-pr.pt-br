---
description: Esta seção contém o material de referência sobre como portar as APIs win32 de banda larga móvel preterida para as APIs Windows Runtime equivalentes.
title: Diretrizes para portar APIs win32 de banda larga móvel para apIs Windows Runtime
ms.topic: reference
ms.date: 08/23/2021
ms.openlocfilehash: 4cbe0415e40f18d372fdd8b9089dbd4afe197b38
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767702"
---
# <a name="guidelines-for-porting-mobile-broadband-win32-apis-to-windows-runtime-apis"></a>Diretrizes para portar APIs win32 de banda larga móvel para apIs Windows Runtime

Esta tabela lista a Windows runtime equivalente para as APIs win32 de banda larga móvel preterida.

| **IMbnConnection** |  Funcionalidade Windows runtime equivalente |
| - | - |
| Conectar | ConnectivityManager.AcquireConnectionAsync |
| Desconectar | ConnectionSession.Close |
| obter \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetActivationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| GetConnectionState | WwanConnectionProfileDetails.GetNetworkRegistrationState |
| GetVoiceCallState | MobileBroadbandNetwork.GetVoiceCallSupport, PhoneCallManager.IsCallActive |
| **IMbnConnectionEvents** | |
| OnConnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState – após a notificação, o estado de registro atual pode ser recuperado de WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnConnectStateChange | NetworkStateChangeEventDetails.HasNewWwanRegistrationState – após a notificação, o estado de registro atual pode ser recuperado de WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnDisconnectComplete | NetworkStateChangeEventDetails.HasNewWwanRegistrationState – após a notificação, o estado de registro atual pode ser recuperado de WwanConnectionProfileDetails.GetNetworkRegistrationState. |
| OnVoiceCallStateChange | PhoneCallManager.CallStateChanged |
| **IMbnConnectionProfile** | |
| Excluir | ConnectionProfile.TryDeleteAsync |
| GetConnectionProfile | NetworkAdapter.GetConnectedProfileAsync |
| GetConnectionProfiles | NetworkInformation.GetConnectionProfiles |
| **IMbnDeviceService** | |
| CloseCommandSession | MobileBroadbandDeviceServiceCommandSession.CloseSession |
| CloseDataSession | MobileBroadbandDeviceServiceDataSession.CloseSession |
| get \_ DeviceServiceID | MobileBroadbandDeviceService.DeviceServiceId |
| OpenCommandSession | MobileBroadbandDeviceService.OpenCommandSession |
| OpenDataSession | MobileBroadbandDeviceService.OpenDataSession |
| QueryCommand | MobileBroadbandDeviceServiceCommandSession.SendQueryCommandAsync |
| QuerySupportedCommands | MobileBroadbandDeviceService.SupportedCommands |
| Setcommand | MobileBroadbandDeviceServiceCommandSession.SendSetCommandAsync |
| WriteData | MobileBroadbandDeviceServiceDataSession.WriteDataAsync |
| **IMbnDeviceServicesContext** | |
| EnumerateDeviceServices | MobileBroadbandDeviceService.SupportedCommands |
| get \_ MaxCommandSize | MobileBroadbandModem.MaxDeviceServiceCommandSizeInBytes |
| get \_ MaxDataSize | MobileBroadbandModem.MaxDeviceServiceDataSizeInByte |
| GetDeviceService | MobileBroadbandModem.GetDeviceService |
| **IMbnDeviceServicesEvents** | |
| OnReadData | MobileBroadbandDeviceServiceDataSession.DataReceived |
| **IMbnInterface** | |
| obter \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| Getconnection | ConnectionSession obtido de AcquireConnectionAsync |
| GetHomeProvider | MobileBroadbandModem.GetCurrentConfigurationAsync |
| GetInterfaceCapability | MobileBroadbandAccount.CurrentDeviceInformation |
| GetReadyState | MobileBroadbandDeviceInformation.NetworkDeviceStatus |
| GetSubscriberInformation | MobileBroadbandAccount.CurrentDeviceInformation |
| InEmergencyMode | MobileBroadbandModem.IsInEmergencyCallMode |
| **IMbnInterfaceEvents** | |
| OnEmergencyModeChange | MobileBroadbandModem.IsInEmergencyCallModeChanged |
| OnReadyStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnSubscriberInformationChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnInterfaceManager** | |
| Getinterface | MobileBroadbandModem.CurrentAccount |
| **IMbnInterfaceManagerEvents** | |
| OnInterfaceArrival | MobileBroadbandAccountWatcher.AccountAdded |
| OnInterfaceRemoval | MobileBroadbandAccountWatcher.Account |
| **IMbnMultiCa portal** | |
| GetCurrentCellularClass | MobileBroadbandDeviceInformation.CellularClass |
| **IMbnMultiCarrierEvents** | |
| OnCurrentCellularClassChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnPin** | |
| Alteração | MobileBroadbandPin.ChangeAsync |
| Desabilitar | MobileBroadbandPin.DisableAsync |
| Habilitar | MobileBroadbandPin.EnableAsync |
| Digite | MobileBroadbandPin.EnterAsync |
| obter \_ PinFormat | MobileBroadbandPin. Format |
| obter \_ PinLengthMax | MobileBroadbandPin. MaxLength |
| obter \_ PinLengthMin | MobileBroadbandPin. MaxLength |
| obter \_ PinMode | MobileBroadbandPin. Enabled |
| obter \_ PinType | MobileBroadbandPin. Type |
| GetPinManager | MobileBroadbandDeviceInformation.PinManager |
| Bloqueá | MobileBroadbandPin.UnblockAsync |
| **IMbnPinManager** | |
| GetPin | MobileBroadbandPinManager.GetPin |
| GetPinList | MobileBroadbandPinManager.SupportedPins |
| GetPinState | MobileBroadbandPin. LockState |
| **IMbnPinManagerEvents** | |
| **IMbnRadio** | |
| obter \_ SoftwareRadioState | Radio. GetRadiosAsync – rádio. Estado |
| SetSoftwareRadioState | Radio. SetStateAsync |
| **IMbnRadioEvents** | |
| OnRadioStateChange | Radio. Estadochanged |
| **IMbnRegistration** | |
| GetAvailableDataClasses | MobileBroadbandDeviceInformation. DataClasses |
| GetCurrentDataClass | MobileBroadbandNetwork.RegisteredDataClass |
| GetPacketAttachNetworkError | MobileBroadbandNetwork.PacketAttachNetworkError |
| Getproviderid | MobileBroadbandNetwork.RegisteredProviderId |
| GetProviderName | MobileBroadbandNetwork.RegisteredProviderName |
| Getregisterstate | MobileBroadbandNetwork.NetworkRegistrationState |
| GetRegistrationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| **IMbnRegistrationEvents** | |
| OnPacketServiceStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnRegisterStateChange | MobileBroadbandNetworkRegistrationStateChange |
| GetSignalStrength | ConnectionProfile.GetSignalBar / MobileBroadbandCellLte.ReferenceSignalReceivedPowerInDBm / MobileBroadbandCellGsm.ReceivedSignalStrengthInDBm |
| **IMbnSignalEvents** | |
| **IMbnSms** | |
| GetSmsConfiguration | SmsDevice2. SmscAddress, SmsDevice2. CellularClass, None para CDMAShortMessageSize e MaxMessageIndex que não são necessários como API pública. |
| SetSmsConfiguration | SmsDevice2. SmscAddress, nenhum dos outros parâmetros tem suporte |
| SmsSendCdma | SendMessageAndGetResultAsync usando CellularClass no ISmsMessageBase |
| SmsSendCdmaPdu | SendMessageAndGetResultAsync usando MessageType e CellularClass em ISmsMessageBase |
| SmsSendPdu | SendMessageAndGetResultAsync usando MessageType em ISmsMessageBase |
| **IMbnSmsConfiguration** | |
| obter \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| obter \_ SmsFormat | SmsDevice2.CellularClass |
| colocar \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| **IMbnSmsEvents** | |
| OnSmsNewClass0Message | SmsMessageRegistration. MessageReceived |
| OnSmsSendComplete | SmsSendMessageResult |
| **IMbnSmsReadMsgPdu** | |
| obter \_ mensagem | SmsTextMessage2. Body |
| obter \_ PduData | SmsTextmessage2. Body |
| **IMbnSmsReadMsgTextCdma** | |
| obter \_ Endereço | SmsTextMessage2. from |
| obter \_ encodingid | SmsTextMessage2. Encoding |
| obter \_ mensagem | SmsTextMessage2. Body |
| obter \_ carimbo de data/hora | SmsTextMessage.2Timestamp |
| **IMbnSubscriberInformation** | |
| obter \_ SimIccID | MobileBroadbandDeviceInformation.SimIccId |
| obter \_ assinante | MobileBroadbandDeviceInformation. subscriberid |
| obter \_ TelephoneNumbers | MobileBroadbandDeviceInformation.TelephoneNumbers |

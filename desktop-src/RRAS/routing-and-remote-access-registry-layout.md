---
title: Layout do registro de roteamento e acesso remoto
description: A sintaxe a seguir mostra um exemplo de layout de registro para o serviço de roteador.
ms.assetid: 5464c2f7-6bb8-4838-939d-d58508715505
keywords:
- Roteamento e acesso remoto do serviço RRAS, roteamento e acesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3388c2a11f69a473a334105d2872872b98b17b4956f12f886e50ada89f406f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027396"
---
# <a name="routing-and-remote-access-registry-layout"></a>Layout do registro de roteamento e acesso remoto

A sintaxe a seguir mostra um exemplo de layout de registro para o serviço de roteador.

``` syntax
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\RasMan 
    \PPP
        \ControlProtocols
            \Builtin
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasppp.dll
            \Chap
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\raschap.dll
        \EAP 
            \<typeID> 
                ConfigCLSID: REG_SZ: <guid> 
                ConfigUiPath: REG_EXPAND_SZ: %SystemRoot%\System32\rastls.dll 
                FriendlyName: REG_SZ: Public Key Based Authentication (EAP-TLS) 
                IdentityUIPath: REG_EXPAND_SZ: %SystemRoot%\System32\rastls.dll 
                InvokePasswordDialog: REG_DWORD: 0 
                InvokeUsernameDialog: REG_DWORD: 0 
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rastls.dll 
            \<typeID> 
                FriendlyName: REG_SZ: MD5 CHAP 
                InvokePasswordDialog: REG_DWORD: 0x1 
                InvokeUsernameDialog: REG_DWORD: 0x1 
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\raschap.dll 
                StandaloneSupported: REG_DWORD: 0 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\RemoteAccess 
    \Accounting 
        \Providers 
            ActiveProvider: REG_SZ: . . .             \<guid>
                ConfigCLSID: REG_SZ: <guid>
                DisplayName: REG_SZ: Radius Accounting
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasrad.dll
                Vendor: REG_SZ: Microsoft
             . . . 
    \Authentication 
        \Providers 
            ActiveProvider: REG_SZ: . . .             \<guid>
                ConfigCLSID: REG_SZ: <guid>
                DisplayName: REG_SZ: Radius Authentication
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasrad.dll
                Vendor: REG_SZ: Microsoft
            \<guid>
                ConfigCLSID: REG_SZ: <guid>
                DisplayName: REG_SZ: NT Authentication
                Path: REG_EXPAND_SZ: %SystemRoot%\System32\rasauth.dll
                Vendor: REG_SZ: Microsoft
             . . . 
    \DemandDialManager
        DLLPath: REG_EXPAND_SZ: . . . 
        < RAS parameters and DDM parameters > 
    \Interfaces
        \0
            Enabled: REG_DWORD: (0/1) 
            InterfaceName: REG_SZ: CorpHQ 
            Type: REG_DWORD: (Internal/Dedicated/Loopback) 
                \IP
                    InterfaceInfo: REG_BINARY: . . . 
                    ProtocolID: REG_DWORD: 0x0021 
                \IPX
                    InterfaceInfo: REG_BINARY: . . . 
                    ProtocolID: REG_DWORD: 0x002B
                . . . 
        \N
            InterfaceName: REG_SZ: IntelEtherExpressPro2 
            . . . 
    \Parameters 
        LANOnlyMode: REG_DWORD: (0/1) 
        ServerFlags: REG_DWORD: . . . 
        ServiceDLL: REG_EXPAND_SZ: %SystemRoot%\System32\mprdim.dll
    \RouterManagers 
        \IP 
            DLLPath: REG_SZ: . . . 
            GlobalInFilter: REG_BSZ: < filter set name > . . . 
            GlobalInfo: REG_BINARY: . . . 
            GlobalInterfaceInfo: REG_BINARY: . . . 
            ProtocolID: REG_DWORD: 0x0021 
            . . . 
            \IPX 
            DLLPath: REG_SZ: . . . 
            GlobalInFilter: REG_BSZ: < filter set name > . . . 
            GlobalInfo: REG_BINARY: . . . 
            GlobalInterfaceInfo: REG_BINARY: . . . 
            ProtocolID: REG_DWORD: 0x002B 
            . . . 
        . . .
 
HKEY_LOCAL_MACHINE\Software\Microsoft 
    \Router 
        \CurrentVersion 
            \RouterManagers 
                \IP 
                    \OSPF 
                        ConfigDll: REG_SZ: ipadmin.dll 
                        DllName: REG_SZ: ospf.dll 
                        ProtocolID: REG_DWORD: 0xD 
                        Title: REG_SZ: Open Shortest Path First 
                    \IPBOOTP
                        . . . 
                    \IPRIP
                        . . . 
                \IPX 
                    \IpxRip 
                        ConfigDll: REG_SZ: ipxadmin.dll 
                        DllName: REG_SZ: IPXRIP.DLL 
                        ProtocolID: REG_DWORD: 0x20000 
                        Title: REG_SZ: RIP for Ipx 
                    \IpxSap
                        . . . 
                    . . . 
            \UIConfigDlls 
                <guid1>: REG_SZ: ifadmin.dll 
                <guid2>: REG_SZ: ipadmin.dll 
                <guid3>: REG_SZ: ipxadmin.dll 
                <guid4>: REG_SZ: ddmadmin.dll
```

Cada Gerenciador de roteador instalado no sistema tem uma chave de registro criada na chave do roteador. A variável DLLPath especifica o local da DLL que corresponde ao Gerenciador de roteador e a variável Protocolid especifica o identificador da família de protocolos para o Gerenciador de roteador.

A chave interfaces é populada com as interfaces que foram adicionadas ao sistema local da configuração do roteador. Cada interface tem um tipo associado (interno, dedicado ou dinâmico) e subchaves para cada Gerenciador de roteador (IP e IPX, por exemplo).

 

 





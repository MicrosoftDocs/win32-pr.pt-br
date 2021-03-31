---
title: Propriedade IMsRdpExtendedSettings Property
description: Contém uma propriedade nomeada.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de propriedade
- Propriedade de propriedade Serviços de Área de Trabalho Remota, interface IMsRdpExtendedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpExtendedSettings, Propriedade Property
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103645612"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>IMsRdpExtendedSettings: Propriedade roperty de:P

Contém uma propriedade nomeada.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a>Valor da propriedade

O valor da propriedade nomeada.

| Nome da propriedade | Tipo de dados | Access | Pode ser alterado após a conexão ser iniciada | Descrição |
|----------|-----------|--------|-----------------------------------------|-------------|
| ConnectToChildSession | **BOOL do VT \_** | Leitura/Gravação | Sim | Definir essa propriedade como **true** faz com que o controle de cliente se conecte à sessão filho no computador local, em vez de um servidor remoto. Se essa propriedade for definida como **true**, você não poderá se conectar a um servidor remoto, pois todas as conexões serão redirecionadas para localhost. Para obter mais informações sobre sessões filho, consulte [sessões filhas](child-sessions.md). |
| DisableCredentialsDelegation | **BOOL do VT \_** | Leitura/Gravação | Não | Se **for true**, as credenciais não serão enviadas ao servidor remoto. |
| EnableFrameBufferRedirection | **BOOL do VT \_** | Leitura/Gravação | Não | Se for **true**, o redirecionamento de buffer de quadro será tentado. Para uma conexão de auto-retorno (o mesmo computador é cliente e servidor), o redirecionamento de buffer de quadro permite que a memória do buffer de quadros seja compartilhada entre as sessões. |
| EnableHardwareMode | **BOOL do VT \_**  | Somente gravação | Não | Se for **true**, será feita uma tentativa de assistência de hardware com a decodificação de gráficos. |
| IgnoreCursors | **BOOL do VT \_** | Somente gravação | Não | Se **for true**, os cursores enviados pelo servidor remoto serão ignorados. |
| ManualClipboardSyncEnabled | **BOOL do VT \_** | Leitura/Gravação | Sim | Definir essa propriedade como **true** significa que as áreas de transferência locais e remotas não serão mantidas automaticamente em sincronia. Em vez disso, a interface [**IMsRdpClipboard**](imsrdpclipboard.md) deve ser usada para sincronizar formatos de área de transferência da área de transferência local para a área de transferência remota e a área de transferência remota para a área de transferência local. |
| ZoomLevel | **_\_UI4 VT_* | Leitura/Gravação | Sim | Implementa o recurso de zoom usando o controle ActiveX RDP. O recurso de zoom está disponível no menu do **sistema** do RDP. A propriedade **ZoomLevel** não tem nenhum efeito no modo RemoteApp e no modo de tela inteira. [**IMsRdpClientAdvancedSettings:: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) e **ZoomLevel** são mutuamente exclusivos. |

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54d38bf7-b1ef-4479-9674-1bd6ea465258<br/> CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpExtendedSettings é definido como 302D8188-0052-4807-806A-362B628F9AC5<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 






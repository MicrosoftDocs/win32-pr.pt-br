---
title: Propriedade IMsTscSecuredSettings StartProgram
description: Especifica o programa a ser iniciado no servidor remoto durante a conexão.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade StartProgram
- Propriedade StartProgram Serviços de Área de Trabalho Remota, interface IMsTscSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsTscSecuredSettings, Propriedade StartProgram
- Propriedade StartProgram Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade StartProgram
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796298"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a>Propriedade IMsTscSecuredSettings:: StartProgram

Especifica o programa a ser iniciado no servidor remoto durante a conexão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a>Valor da propriedade

O nome do novo programa de início. O comprimento máximo dessa cadeia de caracteres é o **\_ caminho máximo**-1 caracteres.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Se o valor dessa propriedade não for definido, o comando do shell do usuário da sessão será executado. O comando do shell será lido a partir do seguinte valor do registro no servidor:

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **shell**

Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings é definido como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 






---
title: Interface IMsTscSecuredSettings
description: Inclui métodos para recuperar e definir as propriedades do Área de Trabalho Remota controle ActiveX que são restritos a zonas de segurança de URL específicas do Internet Explorer. | Interface IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsTscSecuredSettings
- Serviços de Área de Trabalho Remota da interface IMsTscSecuredSettings, descrita
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105784062"
---
# <a name="imstscsecuredsettings-interface"></a>Interface IMsTscSecuredSettings

Inclui métodos para recuperar e definir as propriedades do Área de Trabalho Remota controle ActiveX que são restritos a zonas de segurança de URL específicas do Internet Explorer. As propriedades incluem aquelas que especificam o modo do controle de cliente (modo de tela inteira ou modo de janela) e o programa a ser iniciado após a conexão com o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Esses métodos também estão disponíveis por meio da interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .

## <a name="members"></a>Membros

A interface **IMsTscSecuredSettings** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsTscSecuredSettings** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsTscSecuredSettings** tem essas propriedades.



| Propriedade                                                              | Tipo de acesso           | Descrição                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [**FullScreen**](imstscsecuredsettings-fullscreen.md)<br/>     | Leitura/gravação<br/> | O estado de tela inteira do controle de cliente.<br/>                    |
| [**StartProgram**](imstscsecuredsettings-startprogram.md)<br/> | Leitura/gravação<br/> | O programa a ser iniciado no servidor remoto durante a conexão.<br/> |
| [**WorkDir**](imstscsecuredsettings-workdir.md)<br/>           | Leitura/gravação<br/> | O diretório de trabalho do programa de início.<br/>                     |



 

## <a name="remarks"></a>Comentários

Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações sobre os métodos dessa interface.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


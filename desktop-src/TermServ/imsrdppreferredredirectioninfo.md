---
title: Interface IMsRdpPreferredRedirectionInfo
description: Fornece uma propriedade para controlar o uso de um servidor de redirecionamento.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpPreferredRedirectionInfo
- Serviços de Área de Trabalho Remota da interface IMsRdpPreferredRedirectionInfo, descrita
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454780"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a>Interface IMsRdpPreferredRedirectionInfo

Fornece uma propriedade para controlar o uso de um servidor de redirecionamento.

## <a name="members"></a>Membros

A interface **IMsRdpPreferredRedirectionInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpPreferredRedirectionInfo** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpPreferredRedirectionInfo** tem essas propriedades.



| Propriedade                                                                                               | Tipo de acesso           | Descrição                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**UseRedirectionServerName**](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | Leitura/gravação<br/> | Obtém e define se deve ser usado o nome do servidor de redirecionamento.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 é definido como A9D7038D-B5ED-472e-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 é definido como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpPreferredRedirectionInfo é definido como FDD029F9-9574-4DEF-8529-64B521CCCAA4<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 


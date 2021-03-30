---
title: Propriedade IMsRdpPreferredRedirectionInfo UseRedirectionServerName
description: Obtém e define se deve ser usado o nome do servidor de redirecionamento.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade UseRedirectionServerName
- Propriedade UseRedirectionServerName Serviços de Área de Trabalho Remota, interface IMsRdpPreferredRedirectionInfo
- Serviços de Área de Trabalho Remota de interface IMsRdpPreferredRedirectionInfo, Propriedade UseRedirectionServerName
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644464"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a>Propriedade IMsRdpPreferredRedirectionInfo:: UseRedirectionServerName

Obtém e define se deve ser usado o nome do servidor de redirecionamento.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a>Valor da propriedade

Se deve ser usado o nome do servidor de redirecionamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpPreferredRedirectionInfo é definido como FDD029F9-9574-4DEF-8529-64B521CCCAA4<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 






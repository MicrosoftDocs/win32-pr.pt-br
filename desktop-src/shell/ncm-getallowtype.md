---
description: Recupera os tipos de endereço de rede que um controle de endereço de rede especificado aceita.
title: NCM_GETALLOWTYPE mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11b937ca851f00c51090683db4aebfc3db63cbf83efc95bad7a6f456d8f58988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858805"
---
# <a name="ncm_getallowtype-message"></a>Mensagem \_ NCM GETALLOWTYPE

Recupera os tipos de endereço de rede que um controle de endereço de rede especificado aceita.


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna os tipos de endereço de rede permitidos como uma ou mais das constantes [**\_ NET STRING.**](net-string.md)

## <a name="remarks"></a>Comentários

A máscara retornada é o critério usado para validar um endereço de rede na mensagem [**\_ GETADDRESS do NCM.**](ncm-getaddress.md)

Use essa mensagem apenas para um controle de endereço de rede. Para insinuar, use a **classe msctls \_ numddress definido** em Shellapi.h. Chame [**InitNetworkAddressControl em**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) tempo de executar antes de enviar essa mensagem. Isso inicializa a biblioteca de controles comuns que contém o controle de endereço de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 





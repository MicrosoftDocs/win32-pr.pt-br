---
description: Exibe uma mensagem de erro na dica de balão associada ao controle de endereço de rede.
title: NCM_DISPLAYERRORTIP mensagem (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 046119c93ec6a80fcfcedbd562d04665d5642fd832f2385bab914cc732499e5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111466"
---
# <a name="ncm_displayerrortip-message"></a>Mensagem NCM \_ DISPLAYERRORTIP

Exibe uma mensagem de erro na dica de balão associada ao controle de endereço de rede.


```C++
NCM_DISPLAYERRORTIP

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

Se essa mensagem for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Envie essa mensagem para exibir uma mensagem de erro quando um endereço digitado no controle não for validado em relação aos tipos de endereço de rede permitidos definidos com a mensagem [**\_ NCM SETALLOWTYPE.**](ncm-setallowtype.md) Use a [**mensagem \_ GETADDRESS do NCM**](ncm-getaddress.md) para validar o endereço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NetAddr \_ DisplayErrorTip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 





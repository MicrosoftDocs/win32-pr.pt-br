---
description: Indica se um endereço de rede está de acordo com um tipo e formato especificados.
title: Mensagem de NCM_GETADDRESS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27f5beec56a0125d26cc359f40b5033eda1f035f2dec7666725264ec6fd59ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677964"
---
# <a name="ncm_getaddress-message"></a>\_Mensagem de GETendereço do NCM

Indica se um endereço de rede está de acordo com um tipo e formato especificados.


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*VP* \[ entrada, saída\]
</dt> <dd>Um ponteiro para uma estrutura de <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> para receber informações de endereço de rede no formulário analisado, se o formato de endereço e o tipo no controle especificado por *HWND* forem validados. O aplicativo de chamada é responsável por alocar a memória para essa estrutura.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores do tipo **HRESULT**.



| Código de retorno                                                                                                | Descrição                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Falha do aplicativo de chamada ao alocar uma estrutura de [**\_ endereço NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .<br/> |
| <dl> <dt>**ERRO \_ de \_ buffer insuficiente**</dt> </dl> | O buffer de saída é muito pequeno para conter o endereço de rede analisado.<br/>                           |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>   | A cadeia de caracteres de endereço de rede não é de nenhum tipo especificado.<br/>                                  |
| <dl> <dt>**êxito do erro \_**</dt> </dl>              | A operação foi bem-sucedida.<br/>                                                             |
| <dl> <dt>**\_falso**</dt> </dl>                    | Não há nenhum endereço no controle de endereço de rede para validar.<br/>                           |



 

## <a name="remarks"></a>Comentários

Use a mensagem **NCM \_ GetAddress** para validar um endereço de rede em um controle de endereço de rede em relação a uma máscara de tipo de endereço de rede predefinida. Para criar uma instância, use a classe **msctls \_ netaddress** definida em shellapi. h. Chame [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) em tempo de execução antes de enviar esta mensagem. Isso inicializa a biblioteca de controles comuns que contém o controle de endereço de rede.

Essa mensagem Obtém a cadeia de caracteres de endereço de rede de um controle de endereço de rede, analisa a cadeia de caracteres e verifica se a cadeia de caracteres corresponde a uma máscara de tipo de endereço de rede. Se a cadeia de caracteres corresponder à máscara, a mensagem retornará S \_ OK e retornará a cadeia de caracteres no formulário analisado para o aplicativo de chamada (incluindo o número da porta, o comprimento do prefixo e outras informações de endereço), usando a estrutura de [**\_ endereço do NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) apontada por *VP*. Essa mensagem retornará E \_ INVALIDARG se o aplicativo de chamada falhar ao alocar a estrutura apontada por *VP*.

As representações de endereço IP, versões 4 e 6 (V4/V6) para serviços e redes, bem como endereços e serviços de Internet nomeados usando o formato DNS (sistema de nomes de domínio) são analisadas. Se a cadeia de caracteres de endereço de rede representar um nome de host (DNS) ou serviço nomeado, o valor retornado no membro **PrefixLength** do [**\_ endereço NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) será zero.

Defina a máscara de tipo de endereço de rede usando a mensagem [**NCM \_ SetAllowType**](ncm-setallowtype.md) antes de enviar a macro **\_ GetAddress NCM** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NCM \_ GETallowtype**](ncm-getallowtype.md)
</dt> <dt>

[**Getendereço GetAddr \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 





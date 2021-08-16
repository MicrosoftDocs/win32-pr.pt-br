---
description: Recupera o endereço de origem de um quadro.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Função GetFrameSourceAddress (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4878e08b8d8fb475c0da23d2ed765819fa14a10cd93140c791ed8603b1677584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366313"
---
# <a name="getframesourceaddress-function"></a>Função GetFrameSourceAddress

A **função GetFrameSourceAddress** recupera o endereço de origem de um quadro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* 
</dt> <dd>

Um ponteiro para o quadro para o qual obter um ponteiro.

</dd> <dt>

*Lpaddress* 
</dt> <dd>

Um buffer de retorno que armazena o endereço de origem do quadro.

</dd> <dt>

*AddressType* 
</dt> <dd>

O tipo de endereço pesquisado, como ENDEREÇO TIPO \_ ETHERNET ou IP DE TIPO DE \_ \_ \_ ENDEREÇO.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Os sinalizadores usados para modificar os dados de endereço de origem retornados.



| Valor                                                                                                                                                                                                           | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**NORMALIZAR \_ SINALIZADORES ADDRESSTYPE \_**</dt> </dl>        | Cancela os BITs de roteamento e de grupo.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**ADDRESSTYPE \_ FLAGS \_ BIT \_ REVERSE**</dt> </dl> | Converte endereços de rede de anel de token de volta ao normal.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, *o valor lpAddress* será válido e o valor de retorno será BHERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                                | Descrição                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**PROTOCOLO BHERR \_ \_ NÃO \_ ENCONTRADO**</dt> </dl> | O protocolo especificado pelo parâmetro *AddressType* é inválido para o quadro.<br/> |
| <dl> <dt>**HFRAME \_ INVÁLIDO \_ BHERR**</dt> </dl>      | O *valor do parâmetro hFrame* é inválido.<br/>                                        |



 

## <a name="remarks"></a>Comentários

Um tipo de endereço **DE TIPO DE ENDEREÇO FIND \_ \_ \_ HIGHEST** é permitido. Quando esse tipo de endereço é usado, a função pesquisa o endereço IP IPX, XNS, IP ou VINES antes de retornar o endereço ETHERNET, TOKENRING ou FDDI. Essa abordagem é útil para protocolos e ambientes em que duas NICs podem ser multiplexadas em um único endereço de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





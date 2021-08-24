---
description: Recupera o endereço de destino de um quadro.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Função GetFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d7719392794027567521ce3e9c1bd1caf8ecbf76110f76ad0e54e0dd6549aae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366621"
---
# <a name="getframedestaddress-function"></a>Função GetFrameDestAddress

A função **GetFrameDestAddress** recupera o endereço de destino de um quadro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetFrameDestAddress(
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

Um identificador do quadro para o qual obter um ponteiro.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Um buffer de retorno que armazena o endereço de destino do quadro.

</dd> <dt>

*AddressType* 
</dt> <dd>

Um tipo de endereço, como tipo de \_ endereço \_ Ethernet ou tipo de endereço \_ \_ IP.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Os sinalizadores usados para modificar os dados de endereço de destino retornados.



| Valor                                                                                                                                                                                                           | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**sinalizadores de ADDRESStype \_ \_ NORMALIZE**</dt> </dl>        | Cancela os BITs de grupo e de roteamento.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**sinalizadores de \_ \_ bits \_ invertidos de endereço**</dt> </dl> | Converte endereços de rede de token ring de volta em normal.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de *lpAddress* será válido e o valor de retorno será BHERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                                | Descrição                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_protocolo BHERR \_ não \_ encontrado**</dt> </dl> | O protocolo especificado no parâmetro *AddressType* é inválido para o quadro.<br/> |
| <dl> <dt>**BHERR \_ HFRAME inválida \_**</dt> </dl>      | O valor de *hFrame* é inválido.<br/>                                                  |



 

## <a name="remarks"></a>Comentários

O tipo de endereço localizar tipo de endereço **\_ \_ \_ mais alto** é permitido. Quando esse tipo de endereço é usado, a função procura o endereço IP IPX, XNS, IP ou VINEs antes de retornar o endereço ETHERNET, TOKENRING ou FDDI. Essa abordagem é útil para protocolos e em ambientes em que duas NICs podem ser multiplexada em um único endereço de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





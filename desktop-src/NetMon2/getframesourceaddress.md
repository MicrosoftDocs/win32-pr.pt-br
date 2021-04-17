---
description: Recupera o endereço de origem de um quadro.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Função GetFrameSourceAddress (Netmon. h)
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
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770469"
---
# <a name="getframesourceaddress-function"></a>Função GetFrameSourceAddress

A função **GetFrameSourceAddress** recupera o endereço de origem de um quadro.

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

Um identificador para o quadro para o qual um ponteiro deve ser obtido.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Um buffer de retorno que armazena o endereço de origem do quadro.

</dd> <dt>

*AddressType* 
</dt> <dd>

O tipo de endereço procurado, como tipo de endereço \_ \_ Ethernet ou tipo de \_ endereço \_ IP.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Os sinalizadores usados para modificar os dados de endereço de origem retornados.



| Valor                                                                                                                                                                                                           | Significado                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**sinalizadores de ADDRESStype \_ \_ NORMALIZE**</dt> </dl>        | Cancela os BITs de grupo e de roteamento.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**sinalizadores de \_ \_ bits \_ invertidos de endereço**</dt> </dl> | Converte endereços de rede de token ring de volta em normal.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de *lpAddress* será válido e o valor de retorno será BHERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                                | Descrição                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_protocolo BHERR \_ não \_ encontrado**</dt> </dl> | O protocolo especificado pelo parâmetro *AddressType* é inválido para o quadro.<br/> |
| <dl> <dt>**BHERR \_ HFRAME inválida \_**</dt> </dl>      | O valor do parâmetro *hFrame* é inválido.<br/>                                        |



 

## <a name="remarks"></a>Comentários

É permitido um tipo de endereço de **tipo de endereço \_ \_ \_ mais alto** . Quando esse tipo de endereço é usado, a função procura o endereço IP IPX, XNS, IP ou VINEs antes de retornar o endereço ETHERNET, TOKENRING ou FDDI. Essa abordagem é útil para protocolos e ambientes nos quais duas NICs podem ser multiplexada em um único endereço de servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





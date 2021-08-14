---
description: Usado para liberar memória que foi alocada por uma das funções de provedor de protocolo SSL (protocolo SSL Protocol).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Função SslFreeBuffer (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6121802b8815a2e13fab0f4336420b763fe931a6e022fcce73080adfb01197c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906475"
---
# <a name="sslfreebuffer-function"></a>Função SslFreeBuffer

A função **SslFreeBuffer** é usada para liberar memória que foi alocada por uma das funções de provedor de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pvInput* \[ no\]
</dt> <dd>

Um ponteiro para o buffer de memória a ser liberado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *pdwProviderCount* ou *ppProviderList* é **nulo**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 


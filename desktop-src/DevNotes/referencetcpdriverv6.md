---
description: Obtém uma referência a um objeto de driver TCP v6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: Função ReferenceTcpDriverV6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 7c8fc1a24b812608db74fa16b8dafc323fe48442d61d7d7b35c0d371c0828ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571766"
---
# <a name="referencetcpdriverv6-function"></a>Função ReferenceTcpDriverV6

Obtém uma referência a um objeto de driver TCP v6.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDriverObject* \[ out\]
</dt> <dd>

Um ponteiro para uma estrutura **DRIVER \_ OBJECT.** Para obter mais informações, consulte a documentação do WDK.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela **retornará STATUS \_ SUCCESS.** Se falhar, ele retornará o código de status apropriado.

## <a name="remarks"></a>Comentários

Essa função só pode ser chamada no modo kernel. O chamador deve decrementar a contagem de referência chamando a **função ObDereferenceObject** quando terminar com o objeto .

Essa função é implementada em Driblef.lib, que está disponível para download. Consulte [Windows API de Referência de Driver de Rede](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Driblef.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 





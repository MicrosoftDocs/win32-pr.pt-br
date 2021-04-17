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
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749708"
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

*ppDriverObject* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura de **\_ objeto de driver** . Para obter mais informações, consulte a documentação do WDK.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará o **status \_ êxito**. Se falhar, ele retornará o código de status apropriado.

## <a name="remarks"></a>Comentários

Essa função pode ser chamada somente do modo kernel. O chamador deve decrementar a contagem de referência chamando a função **ObDereferenceObject** quando terminar com o objeto.

Essa função é implementada em Drvref. lib, que está disponível para download. Consulte [biblioteca de API de referência do driver de rede do Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Drvref. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 





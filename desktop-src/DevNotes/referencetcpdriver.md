---
description: Obtém uma referência a um objeto de driver TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: Função ReferenceTcpDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751948"
---
# <a name="referencetcpdriver-function"></a>Função ReferenceTcpDriver

Obtém uma referência a um objeto de driver TCP v4.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
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

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 





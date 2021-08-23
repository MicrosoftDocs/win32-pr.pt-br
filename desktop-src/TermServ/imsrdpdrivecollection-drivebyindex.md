---
title: Propriedade DriveByIndex de IMsRdpDriveCollection
description: Recupera a unidade no índice especificado.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Propriedade DriveByIndex Serviços de Área de Trabalho Remota
- A propriedade DriveByIndex Serviços de Área de Trabalho Remota , interface IMsRdpDriveCollection
- Interface IMsRdpDriveCollection Serviços de Área de Trabalho Remota propriedade , DriveByIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8854bb0b406048d999324a034ebc62b100496c7cf4b5838733e9addd50d42f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000696"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a>Propriedade IMsRdpDriveCollection::D riveByIndex

Recupera a unidade no índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro de interface [**IMsRdpDrive.**](imsrdpdrive.md)

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem-sucedido, **S \_ OK** será retornado. Qualquer outro **valor HRESULT** indica que a chamada falhou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection é definido como 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 






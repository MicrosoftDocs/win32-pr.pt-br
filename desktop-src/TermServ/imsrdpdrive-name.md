---
title: Propriedade Nome do IMsRdpDrive
description: Recupera o nome da unidade.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Nome da propriedade Serviços de Área de Trabalho Remota
- Propriedade name Serviços de Área de Trabalho Remota , interface IMsRdpDrive
- Interface IMsRdpDrive Serviços de Área de Trabalho Remota propriedade , Nome
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bde69814f38c39315a02a76bd52b8c3c38baffc2c0a92601ef383cb60b0bc492
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125636"
---
# <a name="imsrdpdrivename-property"></a>Propriedade IMsRdpDrive::Name

Recupera o nome da unidade.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>Valor da propriedade

O nome da unidade.

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem-sucedido, **S \_ OK** será retornado. Qualquer outro **valor HRESULT** indica que a chamada falhou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpDrive é definido como \_ d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 






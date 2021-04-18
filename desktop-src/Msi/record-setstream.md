---
description: O método SetStream do objeto Record copia o conteúdo do arquivo especificado no campo registro designado como dados de fluxo. Os dados de fluxo não podem ser inseridos em campos temporários.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Método record. SetStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758617"
---
# <a name="recordsetstream-method"></a>Método record. SetStream

O método **SetStream** do objeto [**Record**](record-object.md) copia o conteúdo do arquivo especificado no campo registro designado como dados de fluxo. Os dados de fluxo não podem ser inseridos em campos temporários.

## <a name="syntax"></a>Sintaxe


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*campo* 
</dt> <dd>

Campo obrigatório número do valor dentro do registro, baseado em 1.

</dd> <dt>

*filePath* 
</dt> <dd>

O local do arquivo a ser copiado. Nenhuma tradução de qualquer tipo é executada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 





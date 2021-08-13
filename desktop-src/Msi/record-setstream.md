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
ms.openlocfilehash: de443f2d6802fb74e4b0f05b90ca8d3b3f97e328991fde50ec05ff37c203943c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626966"
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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 





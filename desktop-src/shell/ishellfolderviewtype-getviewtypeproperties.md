---
description: Obtém as propriedades da exibição.
title: 'Método IShellFolderViewType:: GetViewTypeProperties'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967494"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>Método IShellFolderViewType:: GetViewTypeProperties

Obtém as propriedades da exibição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PIDL* \[ no\]
</dt> <dd>

Tipo: **PCUITEMID \_ filho**

UM PIDL.

</dd> <dt>

*pdwFlags* \[ fora\]
</dt> <dd>

Tipo: **DWORD \** _

Um ponteiro para uma variável de inteiro sem sinal que recebe as propriedades da exibição, que indicam o que fazer quando a exibição é selecionada. Os sinalizadores podem ser qualquer combinação dos valores a seguir.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG \_ notificar \_ Create** (0x00000001)


</dt> <dd>

Crie um item de exibição se não existir.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFICAr \_ Resort** (0x00000002)


</dt> <dd>

Reinsira PIDL e reclassifique.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 





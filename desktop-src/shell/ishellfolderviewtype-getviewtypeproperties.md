---
description: Obtém as propriedades da exibição.
title: Método IShellFolderViewType::GetViewTypeProperties
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
ms.openlocfilehash: 57e053321bbd17c90fbe82832cdb01e9acb6994438d22cb72ef62bf1e7143dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220304"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>Método IShellFolderViewType::GetViewTypeProperties

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

*pidl* \[ Em\]
</dt> <dd>

Tipo: **PCUITEMID \_ CHILD**

Um PIDL.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Tipo: **DWORD \***

Um ponteiro para uma variável de inteiro sem sinal que recebe as propriedades de exibição, que indicam o que fazer quando a exibição é selecionada. Os sinalizadores podem ser qualquer combinação dos valores a seguir.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)


</dt> <dd>

Crie o item de exibição se não estiver lá.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)


</dt> <dd>

Reinserir o PIDL e classificar novamente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 





---
description: Subclasses automaticamente e adiciona efeitos 3D a todas as caixas de diálogo no aplicativo.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Função Ctl3dAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 5edc8bafb00d5444f18b61e0600fb075b6a7367c315c2ab1cfe38f911e9a84d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654606"
---
# <a name="ctl3dautosubclass-function"></a>Função Ctl3dAutoSubclass

Subclasses automaticamente e adiciona efeitos 3D a todas as caixas de diálogo no aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hinstApp* 
</dt> <dd>

Um identificador para o aplicativo a ser registrado como um cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** , a menos que uma das condições a seguir exista, caso em que ela retorna **false**:

-   o CTL3D está em execução no Windows versão 3,0 ou anterior.
-   CTL3D não tem espaço disponível em suas tabelas para o aplicativo atual. O CTL3D pode atender até 32 aplicativos ao mesmo tempo.
-   CTL3D não pode instalar seu gancho de CBT.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 

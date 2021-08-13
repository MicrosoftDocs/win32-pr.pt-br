---
description: Abre um volume especificado e inicializa seu objeto de controle de cota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Inimétodo tialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0df879c626ccdac7494077f021c23a6e42b24f0df3aa780d1be8b1af8225527a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455896"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Inimétodo tialize

Abre um volume especificado e inicializa seu objeto de controle de cota.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sPath* 
</dt> <dd>

Tipo: **cadeia de caracteres**

Um valor de cadeia de caracteres que contém o caminho totalmente qualificado do volume a ser inicializado.

</dd> <dt>

*bReadWrite* 
</dt> <dd>

Tipo: **booliano**

Um valor booliano que especifica como o volume deve ser aberto. Defina *bReadWrite* como **true** para acesso de leitura/gravação ou **false** para acesso somente leitura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 





---
description: O método GetError do objeto View retorna o erro de validação e o nome da coluna para a qual o erro ocorreu.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Método View. GetError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ddbed26565598ad58b3605b7c70a9a5bbede3e5282ff4a7fa011df5c56bd8b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038796"
---
# <a name="viewgeterror-method"></a>Método View. GetError

O método **GetError** do objeto [**View**](view-object.md) retorna o erro de validação e o nome da coluna para a qual o erro ocorreu. Na automação, o valor retornado é uma cadeia de caracteres do formato \# \# ColumnName, em que \# \# representa um código de erro de 2 dígitos. Ele retorna o primeiro erro na matriz de erros da exibição; as chamadas subsequentes retornam o próximo valor na matriz de erros. Quando um valor de ' 00 ' é retornado, não existem mais erros e chamadas subseqüentes simplesmente executam um loop na matriz novamente.

## <a name="syntax"></a>Sintaxe


```JScript
View.GetError()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 





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
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749565"
---
# <a name="viewgeterror-method"></a>Método View. GetError

O método **GetError** do objeto [**View**](view-object.md) retorna o erro de validação e o nome da coluna para a qual o erro ocorreu. Na automação, o valor retornado é uma cadeia de caracteres do formato \# \# ColumnName, em que \# \# representa um código de erro de 2 dígitos. Ele retorna o primeiro erro na matriz de erros da exibição; as chamadas subsequentes retornam o próximo valor na matriz de erros. Quando um valor de ' 00 ' é retornado, não existem mais erros e chamadas subseqüentes simplesmente executam um loop na matriz novamente.

## <a name="syntax"></a>Sintaxe


```JScript
View.GetError()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 





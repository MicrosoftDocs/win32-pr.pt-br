---
description: O método SetAsSingleton do objeto SWbemObjectPath força o caminho para endereçar uma instância WMI singleton de uma classe. Uma classe singleton é uma classe que nunca pode ter mais de uma instância.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Método SWbemObjectPath. SetAsSingleton (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4a8a46566990021a4de4fca95b2b524cc7ddc1f5a797d7e3bffd0dc34ee52186
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568256"
---
# <a name="swbemobjectpathsetassingleton-method"></a>Método SWbemObjectPath. SetAsSingleton

O método **SetAsSingleton** do objeto [**SWbemObjectPath**](swbemobjectpath.md) força o caminho para endereçar uma instância WMI singleton de uma classe. Uma classe singleton é uma classe que nunca pode ter mais de uma instância.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md). SWbemObjectPath

## <a name="syntax"></a>Sintaxe


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **SetAsSingleton** , o objeto **Err** pode conter o código de erro abaixo.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                       |
| IID<br/>                      | ISWbemObjectPath de IID \_<br/>                                                        |



 

 





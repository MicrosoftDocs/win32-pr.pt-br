---
description: O método Item do objeto SWbemObjectSet obtém um SWbemObject da coleção.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Método SWbemObjectSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a0d357eda1098bd20e4ebc68f5b959b7ac5ffd4fb46788ffac99d1f18678d6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857215"
---
# <a name="swbemobjectsetitem-method"></a>Método SWbemObjectSet.Item

O **método Item** do objeto [**SWbemObjectSet**](swbemobjectset.md) obtém um [**SWbemObject**](swbemobject.md) da coleção.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obrigatórios. Caminho relativo do objeto a ser recuperado da coleção. Exemplo: Win32 \_ LogicalDisk="C:"

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o [**objeto SWbemObject**](swbemobject.md) solicitado retornará.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método Item,** o **objeto Err** pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Parâmetro inválido foi especificado.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

O item solicitado não foi encontrado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **método Item** pode exigir muito tempo do processador porque a enumeração completa pelo provedor dos elementos do conjunto é necessária para retornar o resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 





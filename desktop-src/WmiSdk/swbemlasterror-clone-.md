---
description: O \_ método clone do objeto SWbemLastError retorna um novo objeto que é um clone do objeto SWbemLastError atual.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Método de SWbemLastError.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 162944eeb4ee7ca0c72102b704e9f75851bbfb41885e6b79e86d1a438487473f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314662"
---
# <a name="swbemlasterrorclone_-method"></a>Método SWbemLastError. Clone \_

O **método \_ clone** do objeto [**SWbemLastError**](swbemlasterror.md) retorna um novo objeto que é um clone do objeto **SWbemLastError** atual.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o **método \_ clone** for bem-sucedido, ele retornará um novo objeto [**SWbemLastError**](swbemlasterror.md) .

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **clone \_** , o objeto **Err** pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o **método \_ clone** para duplicar uma definição ou instância de classe. Esse método é útil quando você precisa fazer backup da cópia original do objeto enquanto modifica uma nova cópia. Além disso, use esse método para criar várias instâncias novas de uma única instância de origem. Por exemplo, use [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) para criar uma única instância inicial e use **SWbemLastError. Clone \_** para produzir rapidamente 100 cópias da instância. Subsequentemente, você pode modificar os objetos, fornecendo valores específicos para cada objeto.

Não é possível usar esse método para converter uma definição de classe em uma instância ou para converter uma instância em uma definição de classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLASTERROR CLSID<br/>                                                        |
| IID<br/>                      | ISWbemLastError de IID \_<br/>                                                         |



 

 





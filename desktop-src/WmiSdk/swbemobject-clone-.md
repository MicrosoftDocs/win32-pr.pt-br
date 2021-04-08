---
description: O \_ método clone do objeto SWbemObject retorna um novo objeto que é um clone do objeto atual.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Método de SWbemObject.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011584"
---
# <a name="swbemobjectclone_-method"></a>Método SWbemObject. Clone \_

O **método \_ clone** do objeto [**SWbemObject**](swbemobject.md) retorna um novo objeto que é um clone do objeto atual.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, esse método retornará um novo objeto [**SWbemObject**](swbemobject.md) .

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ clone** , o objeto **Err** pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

**Nada** foi especificado como parâmetro e não é aceitável nesse uso.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para clonar o objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o **método \_ clone** para duplicar uma definição de classe ou uma instância. Isso é útil quando você precisa da cópia original do objeto para fins de backup enquanto você está modificando uma nova cópia. Da mesma forma, use esse método para criar várias instâncias novas de uma única instância de origem. Por exemplo, use [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) para criar uma única instância inicial e use **SWbemObject. Clone \_** para produzir rapidamente 100 cópias da instância. Subsequentemente, você pode modificar os objetos, dando a cada um valores específicos.

Não é possível usar esse método para converter uma definição de classe em uma instância ou para converter uma instância em uma definição de classe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



 

 





---
description: O método DoAction do objeto Session executa a função de ação correspondente ao nome fornecido.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Método Session. DoAction (myacquire. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c3f6451ec6ef920e6c6414a9396d2c4eeb2102ffc161e1ed91ce996752cd345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629386"
---
# <a name="sessiondoaction-method"></a>Método Session. DoAction

O método **DoAction** do objeto [**Session**](session-object.md) executa a função de ação correspondente ao nome fornecido. Se um nome de ação nulo for fornecido, o mecanismo usará o valor maiúsculo da [Propriedade Action](action.md) como a ação a ser executada. Se nenhum valor de propriedade for definido, a ação padrão será executada, atualmente definida como INSTALL. Esse método retorna uma enumeração de inteiros.

## <a name="syntax"></a>Sintaxe


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*action* 
</dt> <dd>

Nome da cadeia de caracteres necessária para executar. Diferenciar maiúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

As ações que atualizam o sistema, como as ações [InstallFiles](installfiles-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) , não podem ser executadas chamando o método **DoAction** . A exceção a essa regra é se o método **DoAction** for chamado por meio de uma ação personalizada que é agendada na [tabela InstallExecuteSequence](installexecutesequence-table.md) entre as [ações](installfinalize-action.md) [InstallInitialize](installinitialize-action.md) e InstallFinalize. Ações que não atualizam o sistema, como [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), podem ser chamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| Cabeçalho<br/>  | <dl> <dt>Metaacquire. h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





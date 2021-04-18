---
description: O método Sequence do objeto Session abre uma consulta na tabela especificada, ordenando as ações pelos números na coluna sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Método Session. Sequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748967"
---
# <a name="sessionsequence-method"></a>Método Session. Sequence

O método **Sequence** do objeto [**Session**](session-object.md) abre uma consulta na tabela especificada, ordenando as ações pelos números na coluna sequence. Para cada linha buscada, o método [**DoAction**](session-doaction.md) é chamado, desde que qualquer expressão de condição fornecida não seja avaliada como false. Retorna um msiDoActionStatusEnum de enumeração, conforme descrito no método [**DoAction**](session-doaction.md) .

## <a name="syntax"></a>Sintaxe


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*table* 
</dt> <dd>

Nome de cadeia de caracteres necessário da tabela a ser usada para sequenciamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método normalmente é chamado internamente por ações de nível superior.

Uma sequência de ação que contém ações que atualizam o sistema, como as ações [InstallFiles](installfiles-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) , não pode ser executada chamando o método **Sequence** . A exceção a essa regra é se o método **Sequence** for chamado por meio de uma ação personalizada agendada na [tabela InstallExecuteSequence](installexecutesequence-table.md) entre as ações [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md). Ações que não atualizam o sistema, como [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), podem ser chamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





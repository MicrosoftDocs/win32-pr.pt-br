---
description: O método EvaluateCondition do objeto Session avalia uma expressão lógica que contém símbolos e valores. Esse método usa a função MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Método Session. EvaluateCondition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759375"
---
# <a name="sessionevaluatecondition-method"></a>Método Session. EvaluateCondition

O método **EvaluateCondition** do objeto [**Session**](session-object.md) avalia uma expressão lógica que contém símbolos e valores. Esse método usa a função [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .

## <a name="syntax"></a>Sintaxe


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*problema* 
</dt> <dd>

Cadeia de caracteres necessária que contém a expressão lógica. Para obter mais informações, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um inteiro que indica a avaliação da condição.



| Constante                  | Valor | Descrição                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | A condição é avaliada como false.         |
| msiEvaluateConditionTrue  | 1     | A condição é avaliada como true.          |
| msiEvaluateConditionNone  | 2     | Uma expressão condicional não é fornecida. |
| msiEvaluateConditionError | 3     | A condição contém um erro de sintaxe.    |



 

## <a name="remarks"></a>Comentários

Expressões condicionais podem ser usadas para comparar Estados de recursos e componentes. A tabela a seguir mostra o recurso e os Estados de componente que o método EvaluateCondition usa.



| Estado                 | Valor | Descrição                                              |
|-----------------------|-------|----------------------------------------------------------|
| Nulo                  | Nulo  | Nenhuma ação executada no recurso ou componente.                 |
| msiInstallStateAbsent | 2     | O recurso ou componente não está presente.                     |
| msiInstallStateLocal  | 3     | O recurso ou componente está instalado no computador local. |
| msiInstallStateSource | 4     | O recurso ou componente está instalado para ser executado da origem.    |



 

> [!Note]  
> Os Estados não são definidos até que o método [**SetInstallLevel**](session-setinstalllevel.md) seja chamado, seja diretamente ou pela [ação CostFinalize](costfinalize-action.md). Portanto, a verificação de estado só é útil em expressão condicional em uma tabela de sequência de ação.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de instrução condicional](conditional-statement-syntax.md)
</dt> </dl>

 

 





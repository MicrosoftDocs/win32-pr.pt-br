---
description: O método FormatText do objeto Record formata os campos de acordo com o modelo no campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Método record. FormatText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 28170a4d92f656dcd12863eca5c003ccb851772f42de375e8f5f1b61a768ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626976"
---
# <a name="recordformattext-method"></a>Método record. FormatText

O método **FormatText** do objeto [**Record**](record-object.md) formata os campos de acordo com o modelo no campo 0.

## <a name="syntax"></a>Sintaxe


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **FormatText** segue a funcionalidade da função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) se **MsiFormatRecord** recebeu um identificador de instalador nulo como seu primeiro parâmetro. Como resultado, somente os parâmetros de campo de registro são processados e as propriedades não estão disponíveis para substituição.

Por exemplo, uma cadeia de caracteres como "Formatar este campo: \[ 1 \] , formatar esta propriedade: \[ propriedade \] " é resolvida como "Formatar este campo: valor do campo 1, formatar esta propriedade: \[ propriedade \] ".

Os parâmetros que devem ser [formatados](formatted.md) são colocados entre colchetes \[ ... \] . Os colchetes podem ser iterados porque as substituições são resolvidas de dentro para fora.

Se uma parte da cadeia de caracteres estiver entre chaves {} e não contiver colchetes, ela permanecerá inalterada, incluindo as chaves.

Observação no caso de [ações personalizadas de execução adiada](deferred-execution-custom-actions.md), o **FormatText** dá suporte apenas a um conjunto limitado de propriedades: as propriedades CustomActionData e ProductCode. Para obter mais informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[Binário](formatted.md)
</dt> <dt>

[Tipos de dados de coluna](column-data-types.md)
</dt> </dl>

 

 





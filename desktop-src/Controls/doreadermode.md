---
title: Função doreadermode
description: Habilita o modo de leitura em uma janela.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Controles do Windows da função doreadermode
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456061"
---
# <a name="doreadermode-function"></a>Função doreadermode

\[O **Doreadermode** está disponível por meio do Windows XP com Service Pack 2 (SP2). Ele pode não estar disponível em versões subsequentes.\]

Habilita o modo de leitura em uma janela.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*prmi* \[ no\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Um ponteiro para uma estrutura [**READERMODEINFO**](readermodeinfo.md) que contém informações de inicialização para o modo leitor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O modo leitor é ativado por meio de dispositivos com suporte com um clique do mouse, normalmente usando um terceiro botão do mouse ou roda de rolagem. O movimento subsequente do mouse em uma área especificada rola o conteúdo dessa área em vez de mover um ponteiro. Fora dessa área, o ponteiro do mouse é exibido e opera normalmente. Um segundo clique no botão ou na roda de rolagem libera o dispositivo do modo leitor.

> [!Note]  
> Essa função não é declarada em nenhum cabeçalho público. Para usá-lo, você deve acessá-lo como ordinal 383 de Comctl32.dll.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 4,72 ou posterior)</dt> </dl> |



 

 






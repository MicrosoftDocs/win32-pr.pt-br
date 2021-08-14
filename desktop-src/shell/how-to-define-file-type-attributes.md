---
description: Definindo atributos de tipo de arquivo no Registro.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Como definir atributos de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0a89f5770b55521ccdf51859bdde69ed58d05f864385e46f1d76e482319c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223570"
---
# <a name="how-to-define-file-type-attributes"></a>Como definir atributos de tipo de arquivo

Atribuir atributos de tipo de arquivo a um ProgID associado permite controlar alguns aspectos do comportamento do tipo de arquivo. Antes do Windows Vista, esses atributos podem permitir que você limite  a extensão até a qual o usuário pode usar a guia de propriedades Opções de Pasta para modificar vários aspectos do tipo de arquivo, como seu ícone ou verbos.

Atributos de tipo de arquivo são sinalizadores binários especificados como **valores REG \_ DWORD** ou **REG \_ BINARY** na subkey ProgID associada do tipo de arquivo.

Para atribuir atributos para um tipo de arquivo, siga estas etapas.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Adicione uma entrada EditFlags à sub-chave ProgID associada do tipo de arquivo.

### <a name="step-2"></a>Etapa 2:

De definir a entrada como o valor de atributo apropriado.

O exemplo a seguir mostra os atributos FTA \_ NoRemove (0x00000010) e FTA NoNewVerb (0x00000020) definidos para o tipo de arquivo \_ .myp.

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>Comentários

Os sinalizadores podem ser combinados com um OR lógico para formar o valor de atributo único.

Para obter uma lista de possíveis atributos de tipo de arquivo e seus valores hexadecimais e mais detalhes sobre como recuperar e definir esses valores programaticamente, consulte [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).

 

 




---
description: no Windows 7 e posterior, você pode usar a entrada subcomandos no registro para criar menus em cascata usando o procedimento fornecido neste tópico.
title: Criar menus em cascata com a entrada de registro de subcomandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f12eb473d45a3d3aef1b7cf8e7f6cc51a0d97aa5b9e60ee39681c80af459988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111796"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Como criar menus em cascata com a entrada de registro de subcomandos

no Windows 7 e posterior, você pode usar a entrada subcomandos no registro para criar menus em cascata usando o procedimento fornecido neste tópico.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Crie uma nova subchave em **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shell**, em que *ProgID* é o tipo de arquivo para o qual você deseja adicionar um menu em cascata. Você pode nomear essa nova subchave como desejar. Para o restante deste tópico, vamos chamá-lo de *CascadeMenu*, conforme mostrado no exemplo a seguir.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Etapa 2:

Adicione uma entrada denominada "MUIVerb", do tipo **reg \_ sz** ou **reg \_ Expand \_ sz**, à subchave *CascadeMenu* . Atribua essa entrada a um valor de cadeia de caracteres como "menu de teste em cascata". Normalmente, essa cadeia de caracteres é fornecida como uma referência de recurso no formato " @file , recurso". O valor (padrão) da subchave *CascadeMenu* não deve ser definido.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Etapa 3:

Adicione uma entrada denominada "subcomandos", do tipo **reg \_ sz** ou **reg \_ Expand \_ sz**, à subchave *CascadeMenu* . Atribua essa entrada a uma lista delimitada por ponto-e-vírgula dos verbos que devem aparecer no menu, na ordem desejada de aparência.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Etapa 4:

Preencha a subchave **CommandStore** com implementações de verbo para qualquer método de implementação de verbo estático personalizado que você usou em sua entrada de subcomandos; por exemplo:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando menus em cascata estáticos](creating-static-cascading-menus.md)
</dt> </dl>

 

 




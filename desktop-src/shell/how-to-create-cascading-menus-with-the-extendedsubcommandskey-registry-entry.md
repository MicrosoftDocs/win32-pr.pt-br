---
description: No Windows 7 e posterior, você pode usar a subchave ExtendedSubCommandsKey para criar menus em cascata estendidos.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Criar menus em cascata com a entrada de registro ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662160"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Como criar menus em cascata com a entrada de registro ExtendedSubCommandsKey

No Windows 7 e posterior, você pode usar a subchave **ExtendedSubCommandsKey** para criar menus em cascata estendidos.

A captura de tela a seguir é um exemplo de um menu estendido em cascata.

![captura de tela mostrando o menu em cascata estendida para dispositivos](images/file-assoc/extendedsubcommandskey.png)

Como **a \_ \_ raiz das classes hKey** é uma combinação de **HKEY \_ Current \_ User** e **HKEY \_ local \_ Machine**, você pode registrar os subverbors na subchave **HKEY \_ Current \_ User** \\ **software** \\ **classes** . A vantagem disso é que a permissão elevada não é necessária. Outras associações de arquivo podem reutilizar esse conjunto inteiro de verbos especificando a mesma subchave **ExtendedSubCommandsKey** . Se você não precisar reutilizar esse conjunto de verbos, poderá listar os verbos sob o pai. Nesse caso, verifique se o valor padrão do pai está vazio, conforme ilustrado no exemplo de entrada do registro nesta seção.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Crie uma subchave em **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shell** \\ *CascadeMenuKey* e dê ao CascadeMenuKey um nome como *CascadeTest*, por exemplo. Em seguida, adicione uma entrada MUIVerb do tipo **reg \_ sz** e dê a ele um nome como Test Cascade menu 2, conforme ilustrado no exemplo de registro a seguir.

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a>Etapa 2:

Na subchave *CascadeTest* que você criou, adicione uma subchave **ExtendedSubCommandsKey** e, em seguida, adicione os subcomandos de documento (do tipo **reg \_ sz**); por exemplo:

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

Verifique se o valor padrão da subchave *Test Cascade do menu 2* está vazio e mostrado como **(valor não definido)**.

### <a name="step-3"></a>Etapa 3:

Preencha os subverbos usando qualquer uma das seguintes implementações de verbo estático. Observe que a subchave CommandFlags representa os valores de EXPCMDFLAGS. Se você quiser adicionar um separador antes ou depois do item de menu em cascata, use ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40). Para obter uma descrição desses sinalizadores do Windows 7 e posterior, consulte [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE funciona apenas para os itens de menu de nível superior. MUIVerb é do tipo **reg \_ sz** e CommandFlags é do tipo **reg \_ DWORD**.

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a>Comentários

A captura de tela a seguir é uma ilustração dos exemplos de entrada de chave do registro anterior.

![captura de tela mostrando um exemplo de um menu em cascata mostrando as opções do bloco de notas e do WordPad](images/file-assoc/testcascademenu2.png)

 

 




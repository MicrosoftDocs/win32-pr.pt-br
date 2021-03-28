---
description: Como implementar e registrar um manipulador drop.
title: Como criar manipuladores drop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169432"
---
# <a name="how-to-create-drop-handlers"></a>Como criar manipuladores drop

Por padrão, os arquivos não são drop targets. Você pode tornar os membros de um [tipo de arquivo](fa-file-types.md) em drop targets implementando e registrando um *manipulador drop*.

Se um manipulador drop for registrado para um tipo de arquivo, ele será chamado sempre que um objeto for arrastado ou descartado em um membro do tipo de arquivo. O Shell gerencia a operação chamando os métodos apropriados na interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do manipulador.

Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md). Este documento se concentra nesses aspectos da implementação que são específicos para descartar manipuladores.

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-drop-handlers"></a>Etapa 1: implementando manipuladores drop

Como todos os manipuladores de extensão do Shell, os manipuladores de descarte são objetos COM (Component Object Model) em processo implementados como DLLs. Eles exportam duas interfaces além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

O Shell Inicializa o manipulador por meio de sua interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Ele usa essa interface para solicitar o identificador de classe do manipulador (CLSID) e fornece o nome do arquivo. Para obter uma discussão geral sobre como implementar manipuladores de extensão de Shell, incluindo a interface **IPersistFile** , consulte [criando manipuladores de extensão de shell](handlers.md).

Depois que o manipulador drop é inicializado, o Shell chama o método apropriado na interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do manipulador.

### <a name="step-2-registering-drop-handlers"></a>Etapa 2: Registrando manipuladores drop

Os manipuladores de descarte são registrados sob a subchave deste tipo de arquivo.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Crie uma subchave de **DropHandler** chamada para o manipulador e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID CLSID do manipulador. Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](handlers.md).

O exemplo a seguir ilustra as entradas do registro que habilitam um manipulador drop para um tipo de arquivo example. MYP.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criar Manipuladores de Extensão de Shell](handlers.md)
</dt> <dt>

[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 

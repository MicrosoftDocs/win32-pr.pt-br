---
description: Como implementar e registrar um manipulador de soltar.
title: Como criar manipuladores de soltar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34c06aa3eae1892b5b86ce3a0f3b1198be41cd2f9dda5c9bd0956b40a53146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223580"
---
# <a name="how-to-create-drop-handlers"></a>Como criar manipuladores de soltar

Por padrão, os arquivos não são destinos de soltar. Você pode tornar os membros de um tipo [de arquivo](fa-file-types.md) em destinos de soltar implementando e registrando um manipulador *de soltar*.

Se um manipulador de soltar for registrado para um tipo de arquivo, ele será chamado sempre que um objeto for arrastado ou descartado em um membro do tipo de arquivo. O Shell gerencia a operação chamando os métodos apropriados na interface [**IDropTarget do**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) manipulador.

Os procedimentos gerais para implementar e registrar um manipulador de extensão do Shell são discutidos em Criando manipuladores de [extensão do Shell.](handlers.md) Este documento se concentra nos aspectos da implementação que são específicos para soltar manipuladores.

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-drop-handlers"></a>Etapa 1: Implementando manipuladores de soltar

Como todos os manipuladores de extensão do Shell, os manipuladores de soltar são objetos COM (Component Object Model em processo) implementados como DLLs. Eles exportam duas interfaces além [**de IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

O Shell inicializa o manipulador por meio de sua interface [**IPersistFile.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Ele usa essa interface para solicitar o CLSID (identificador de classe) do manipulador e fornece o nome do arquivo. Para uma discussão geral sobre como implementar manipuladores de extensão do Shell, incluindo a interface **IPersistFile,** consulte [Criando manipuladores de extensão do Shell.](handlers.md)

Depois que o manipulador de soltar é inicializado, o Shell chama o método apropriado na interface [**IDropTarget do**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) manipulador.

### <a name="step-2-registering-drop-handlers"></a>Etapa 2: Registrando manipuladores de soltar

Manipuladores de soltar são registrados na sub-chave desse tipo de arquivo.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Crie uma sub-chave de **DropHandler** chamada para o manipulador e de definir o valor padrão da sub-chave como a forma de cadeia de caracteres do GUID CLSID do manipulador. Para uma discussão geral sobre como registrar manipuladores de extensão do Shell, consulte [Criando manipuladores de extensão do Shell.](handlers.md)

O exemplo a seguir ilustra as entradas do Registro que habilitam um manipulador de soltar para um tipo de arquivo .myp de exemplo.

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

[**Idroptarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**Ipersistfile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 

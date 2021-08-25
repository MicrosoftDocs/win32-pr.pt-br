---
description: Estendendo a área de transferência com manipuladores de formato de dados personalizados.
title: Como criar manipuladores de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a3761b4dc8ce3e7d50d967d2267971537d3609e7a7cf76785623734558adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715046"
---
# <a name="how-to-create-data-handlers"></a>Como criar manipuladores de dados

Quando um arquivo é copiado para a área de transferência ou arrastado e descartado, o Shell cria um objeto de dados que dá suporte a uma variedade de formatos de área [de transferência padrão.](dragdrop.md) Para arquivos que são de um tipo de arquivo específico, você pode estender os formatos de área de transferência disponíveis implementando e registrando um manipulador *de dados*. Quando um arquivo do tipo de arquivo é transferido, o Shell delega chamadas à interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados para o manipulador de dados se um dos formatos personalizados for usado.

Os procedimentos gerais para implementar e registrar um manipulador de extensão do Shell são discutidos em Criando manipuladores de [extensão do Shell.](handlers.md) Este documento se concentra nos aspectos da implementação que são específicos para manipuladores de dados.

-   [Implementando manipuladores de dados](#step-1-implementing-data-handlers)
-   [Registrando manipuladores de dados](#step-2-registering-data-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-data-handlers"></a>Etapa 1: Implementando manipuladores de dados

Como todos os manipuladores de extensão do Shell, os manipuladores de dados são objetos COM (Component Object Model em processo) implementados como DLLs. Eles exportam duas interfaces além [**de IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDataObject.**](/windows/win32/api/objidl/nn-objidl-idataobject)

O Shell inicializa o manipulador por meio de sua interface [**IPersistFile.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Ele usa essa interface para solicitar o CLSID (identificador de classe) do manipulador e fornece o nome do arquivo. Para uma discussão geral sobre como implementar manipuladores de extensão do Shell, incluindo a interface **IPersistFile,** consulte [Criando manipuladores de extensão do Shell.](handlers.md)

Depois que o manipulador de dados é inicializado, o Shell delega chamadas do objeto de dados para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do manipulador se um dos formatos personalizados for usado.

### <a name="step-2-registering-data-handlers"></a>Etapa 2: Registrando manipuladores de dados

Os manipuladores de dados são registrados na sub-chave *ProgID* do tipo de arquivo, conforme mostrado aqui: **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\ **shellex** \\ **DataHandler**

Crie uma sub-chave chamada para o manipulador em **DataHandler** e de definir o valor padrão da sub-chave desse manipulador para a forma de cadeia de caracteres do GUID CLSID do manipulador. Para uma discussão geral sobre como registrar manipuladores de extensão do Shell, consulte [Criando manipuladores de extensão do Shell.](handlers.md)

O exemplo a seguir ilustra as entradas do Registro que habilitam um manipulador de dados para um tipo de arquivo .myp de exemplo.

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criar Manipuladores de Extensão de Shell](handlers.md)
</dt> <dt>

[**Ipersistfile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**Idataobject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 

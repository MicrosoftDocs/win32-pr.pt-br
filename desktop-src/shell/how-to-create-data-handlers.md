---
description: Estendendo a área de transferência com manipuladores de formato de dados personalizados.
title: Como criar manipuladores de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988984"
---
# <a name="how-to-create-data-handlers"></a>Como criar manipuladores de dados

Quando um arquivo é copiado para a área de transferência ou arrastado e descartado, o Shell cria um objeto de dados que dá suporte a uma variedade de [formatos de área de transferência](dragdrop.md)padrão. Para arquivos que são de um tipo de arquivo específico, você pode estender os formatos de área de transferência disponíveis implementando e registrando um *manipulador de dados*. Quando um arquivo do tipo de arquivo for transferido, o Shell delegará chamadas para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados para o manipulador de dados se um dos formatos personalizados for usado.

Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md). Este documento se concentra nesses aspectos da implementação que são específicos de manipuladores de dados.

-   [Implementando manipuladores de dados](#step-1-implementing-data-handlers)
-   [Registrando manipuladores de dados](#step-2-registering-data-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-data-handlers"></a>Etapa 1: implementando manipuladores de dados

Como todos os manipuladores de extensão do Shell, os manipuladores de dados são objetos COM (Component Object Model) em processo implementados como DLLs. Eles exportam duas interfaces além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).

O Shell Inicializa o manipulador por meio de sua interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Ele usa essa interface para solicitar o identificador de classe do manipulador (CLSID) e fornece o nome do arquivo. Para obter uma discussão geral sobre como implementar manipuladores de extensão de Shell, incluindo a interface **IPersistFile** , consulte [criando manipuladores de extensão de shell](handlers.md).

Depois que o manipulador de dados for inicializado, o Shell delegará chamadas do objeto de dados para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do manipulador se um dos formatos personalizados for usado.

### <a name="step-2-registering-data-handlers"></a>Etapa 2: Registrando manipuladores de dados

Os manipuladores de dados são registrados na subchave *ProgID* do tipo de arquivo, conforme mostrado aqui: **HKEY \_ classes \_ raiz** \\ *ProgID* \\ **shellex** \\ **DataHandler**

Crie uma subchave chamada para o manipulador em **DataHandler** e defina o valor padrão da subchave desse manipulador como a forma de cadeia de caracteres do GUID CLSID do manipulador. Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](handlers.md).

O exemplo a seguir ilustra as entradas do registro que habilitam um manipulador de dados para um tipo de arquivo. MYP de exemplo.

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

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 

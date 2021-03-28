---
description: Descreve como criar um manipulador para atribuições de ícone personalizado.
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: Como criar manipuladores de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967912"
---
# <a name="how-to-create-icon-handlers"></a>Como criar manipuladores de ícone

Um [tipo de arquivo](fa-file-types.md) geralmente tem um ícone personalizado associado a ele, para tornar seus membros facilmente reconhecíveis no Windows Explorer. A maneira mais simples de atribuir um ícone personalizado a um tipo de arquivo é registrar o arquivo do ícone. No entanto, um ícone registrado dessa maneira será o mesmo para todos os membros do tipo de arquivo. Você pode ter muito mais flexibilidade para atribuir ícones aos membros do tipo de arquivo implementando um *manipulador de ícones*.

Um manipulador de ícones é um tipo de manipulador de extensão de shell que permite atribuir ícones dinamicamente aos membros de um tipo de arquivo. Toda vez que um arquivo do tipo é exibido, o Shell consulta o manipulador para o ícone apropriado. Por exemplo, um manipulador de ícones pode atribuir ícones diferentes a diferentes membros do tipo de arquivo ou variar o ícone com base no estado atual do arquivo.

Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](handlers.md). Este documento se concentra nesses aspectos da implementação que são específicos para manipuladores de ícones.

-   [Implementando manipuladores de ícone](#step-1-implementing-icon-handlers)
-   [Implementando a interface IExtractIcon](#step-2-implementing-the-iextracticon-interface)
-   [Registrando manipuladores de ícone](#step-3-registering-icon-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="instructions"></a>Instruções

### <a name="step-1-implementing-icon-handlers"></a>Etapa 1: implementando manipuladores de ícone

Como todos os manipuladores de extensão do Shell, os manipuladores de ícone são objetos COM (Component Object Model) em processo implementados como DLLs. Eles devem exportar duas interfaces além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

O Shell Inicializa o manipulador por meio de sua interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Ele usa essa interface para solicitar o identificador de classe do manipulador (CLSID) e fornece o nome do arquivo. O restante da operação ocorre por meio da interface [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) . Para obter uma discussão geral sobre como implementar manipuladores de extensão de Shell, incluindo a interface **IPersistFile** , consulte [criando manipuladores de extensão de shell](handlers.md). O restante deste documento discute como implementar a interface **IExtractIcon** .

### <a name="step-2-implementing-the-iextracticon-interface"></a>Etapa 2: implementando a interface IExtractIcon

Depois que a interface é inicializada, o Shell usa a interface [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) do manipulador para solicitar o ícone apropriado. A interface tem dois métodos: [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) e [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Os ícones são identificados por sua localização no sistema de arquivos. O método [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) é chamado para solicitar essas informações. Defina o parâmetro *szIconFile* como o nome do arquivo. Se houver mais de um ícone no arquivo, defina *piIndex* como o índice do ícone. Atribua valores apropriados às duas variáveis de sinalizador. Se você não quiser especificar um nome de arquivo ou se não quiser que o Shell Extraia o ícone, defina o sinalizador Gil não **\_ filename** no parâmetro *pwFlags* . Você não precisa atribuir um valor a *szIconFile*, mas o manipulador deve fornecer identificadores de ícone quando o Shell chama [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Se você retornar um nome de arquivo, o Shell normalmente tentará carregar o ícone de seu cache. Para evitar o carregamento de um ícone armazenado em cache, defina o sinalizador **Gil \_ DONTCACHE** no parâmetro *pwFlags* . Se um ícone armazenado em cache não for carregado, o Shell chamará [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) para solicitar o identificador de ícone.

Se um arquivo e um índice forem especificados por [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation), eles serão passados para [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) nos parâmetros *pszFile* e *nIconIndex* , respectivamente. Se um nome de arquivo for fornecido, o manipulador poderá retornar S \_ false para que o Shell Extraia o ícone. Caso contrário, seu manipulador deve extrair ou produzir ícones grandes e pequenos e atribuir seus identificadores HICON aos parâmetros *phiconLarge* e *phiconSmall* . O Shell adiciona os ícones ao seu cache para agilizar chamadas subsequentes para o manipulador.

### <a name="step-3-registering-icon-handlers"></a>Etapa 3: Registrando manipuladores de ícone

Ao [registrar estaticamente um ícone](icon.md) para um tipo de [arquivo](fa-file-types.md), você cria uma subchave **DefaultIcon** sob o ProgID para o tipo de arquivo. Seu valor padrão é definido como o arquivo que contém o ícone. Para registrar um manipulador de ícones, você ainda deve ter a subchave **DefaultIcon** , mas seu valor padrão deve ser definido como "%1". Adicione uma subchave **IconHandler** à subchave **shellex** da subchave ProgID e defina seu valor padrão como a forma de cadeia de caracteres do GUID CLSID do manipulador. Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](handlers.md).

O exemplo a seguir modifica a entrada do registro de [personalização de ícones](icon.md) para que o tipo de arquivo. MYP agora use um manipulador de menu de atalho em vez de um ícone estaticamente definido.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = %1
      Shellex
         IconHandler
            (Default) = {The handler's CLSID GUID}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criar Manipuladores de Extensão de Shell](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)
</dt> </dl>

 

 

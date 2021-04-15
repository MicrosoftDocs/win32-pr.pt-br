---
title: Criando manipuladores de coluna
description: A exibição de detalhes no Windows Windows Explorer normalmente exibe várias colunas padrão.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- manipuladores de coluna
- registrar, manipuladores de coluna
- GetColumnInfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940796e75f29ba0fcfa025d9a56267e14bdff38f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104569754"
---
# <a name="creating-column-handlers"></a>Criando manipuladores de coluna

\[Esse recurso tem suporte apenas no Windows XP ou anterior. \]

A exibição de detalhes no Windows Windows Explorer normalmente exibe várias colunas padrão. Cada coluna lista informações, como o tamanho ou o tipo do arquivo, para cada arquivo na pasta atual. Ao implementar e registrar um manipulador de colunas, você pode disponibilizar colunas personalizadas para exibição.

Os procedimentos gerais para implementar e registrar um manipulador de extensão de shell são discutidos na [criação de manipuladores de extensão de shell](/windows/desktop/shell/handlers). Este documento se concentra nesses aspectos da implementação que são específicos para manipuladores de coluna.

Os tópicos a seguir são discutidos.

-   [Como funcionam os manipuladores de coluna](#how-column-handlers-work)
-   [Registrando manipuladores de coluna](#registering-column-handlers)
-   [Implementando manipuladores de coluna](#implementing-column-handlers)
    -   [O método Initialize](#the-initialize-method)
    -   [O método GetColumnInfo](#the-getcolumninfo-method)
    -   [O método GetItemData](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Como funcionam os manipuladores de coluna

A ilustração a seguir mostra o Windows Explorer no modo de exibição detalhes.

![captura de tela do Windows Explorer no modo de exibição detalhes](images/columnproviderhandler1.jpg)

Com o Windows 2000, a pasta também pode oferecer suporte a várias colunas que, por padrão, não são exibidas. O usuário pode exibir colunas adicionais clicando com o botão direito do mouse em um dos cabeçalhos de coluna e selecionando o comando **mais...** no menu. Será exibida uma caixa de diálogo que lista as colunas disponíveis para a pasta e permite que o usuário Selecione quais colunas exibir. A ilustração a seguir mostra essa caixa de diálogo para o exemplo anterior.

![captura de tela do Windows Explorer com a caixa de diálogo escolher detalhes exibida](images/columnproviderhandler2.jpg)

Ao criar um manipulador de colunas, você pode criar colunas personalizadas e adicioná-las a essa lista. Por exemplo, uma coleção de arquivos que contêm música pode usar um manipulador de coluna para exibir colunas que listam o artista e a parte contida em cada arquivo.

Um manipulador de coluna é um objeto global que é chamado toda vez que o Windows Explorer exibe a exibição de detalhes. No entanto, os manipuladores de coluna normalmente são usados para exibir colunas personalizadas somente para membros de um determinado [tipo de arquivo](/windows/desktop/shell/fa-file-types). Antes de exibir a exibição de detalhes, o Windows Explorer consulta todos os manipuladores de coluna registrados para suas características de coluna. Se o usuário tiver selecionado uma das colunas do manipulador, o Windows Explorer consultará o manipulador para os dados associados. Quando um manipulador de coluna receber uma solicitação de dados, ele o fornecerá se o arquivo for um membro de seu tipo com suporte. Caso contrário, ele ignora a solicitação retornando S \_ false.

## <a name="registering-column-handlers"></a>Registrando manipuladores de coluna

Os manipuladores de coluna são registrados na subchave a seguir.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Crie uma subchave de **ColumnHandlers** chamada com a forma de cadeia de caracteres do GUID de identificador de classe (CLSID) do manipulador. Para obter uma discussão geral sobre como registrar manipuladores de extensão de Shell, consulte [criando manipuladores de extensão de shell](/windows/desktop/shell/handlers). O exemplo a seguir ilustra como registrar um manipulador de coluna.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implementando manipuladores de coluna

Como todos os manipuladores de extensão do Shell, os manipuladores de coluna são objetos COM (Component Object Model) em processo implementados como DLLs. Eles exportam a interface [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) além de [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

O Windows Explorer chama os três métodos exportados pelo [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) para solicitar as informações necessárias para exibir a coluna. O procedimento usado pelo Windows Explorer é:

1.  Chame [**IColumnProvider:: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) para especificar a pasta que está prestes a ser exibida.
2.  Chame [**IColumnProvider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) para recuperar o identificador e as características da coluna.
3.  Se a coluna tiver sido selecionada pelo usuário, chame [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) para cada arquivo na pasta para recuperar os dados que pertencem à entrada de coluna do arquivo.

### <a name="the-initialize-method"></a>O método Initialize

O Windows Explorer chama [**IColumnProvider:: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) para inicializar o manipulador de colunas. O método tem três parâmetros, mas somente *wszFolder* está sendo usado. Ele é definido para a pasta cuja exibição de detalhes está prestes a ser exibida. Armazene o nome da pasta para uso posterior e inicialize o objeto do manipulador conforme necessário.

### <a name="the-getcolumninfo-method"></a>O método GetColumnInfo

O Windows Explorer Next chama [**IColumnProvider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) para solicitar o identificador e as características da coluna. Ele passa um índice para a coluna no parâmetro *dwIndex* . Esse índice é um valor arbitrário que é usado para enumerar colunas. O Windows Explorer também passa um ponteiro para uma estrutura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) . Essa estrutura é usada para retornar o identificador e as características da coluna. **IColumnProvider:: GetColumnInfo** deve atribuir valores apropriados aos membros da estrutura e retornar.

As colunas são identificadas por sua ID de conjunto de propriedades OLE (FMTID) e uma ID de propriedade associada (PID). O primeiro membro da estrutura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) , **scid**, é um ponteiro para uma estrutura [**SHCOLUMNID**](/windows/desktop/shell/objects) que é usada para identificar a coluna. Seu membro **fmtid** mantém o fmtid da coluna e seu membro **PID** contém o PID da coluna. Por exemplo, um par padrão de FMTID/PID que normalmente é usado para identificar colunas é a PID do autor do conjunto de propriedades de informações resumidas.

Se possível, seu manipulador deve usar FMTIDs e PIDs existentes para identificar a coluna à qual ele dá suporte. Se você usar uma estrutura [**SHCOLUMNID**](/windows/desktop/shell/objects) personalizada, a coluna exibirá dados somente para os arquivos com suporte no manipulador. Se a pasta contiver outros arquivos, suas entradas ficarão em branco. Se uma pasta contiver arquivos de mais de um tipo de arquivo, usar valores padrão de FMTID/PID poderá tornar possível mesclar dados de diferentes tipos na mesma coluna.

Defina o membro **VT** como o [](/windows/win32/api/oaidl/ns-oaidl-variant)   tipo de variante dos dados que você deseja exibir na coluna. O tipo mais comumente usado é VT \_ LPStr, pois a maioria das colunas exibe seus dados como cadeias de caracteres. Os membros restantes da estrutura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) são usados para definir as características da coluna. Atribua valores conforme apropriado.

### <a name="the-getitemdata-method"></a>O método GetItemData

Se a coluna do manipulador de coluna tiver sido selecionada, o Windows Explorer chamará [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) para cada arquivo na pasta a ser exibida. O parâmetro *pscid* é um ponteiro para uma estrutura [**SHCOLUMNID**](/windows/desktop/shell/objects) que identifica a coluna. O parâmetro *pscd* aponta para uma estrutura [**SHCOLUMNDATA**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) que identifica o arquivo específico.

O parâmetro *pvarData* retorna os dados que devem ser exibidos na coluna do manipulador para o arquivo especificado por *pscd*. Se esse arquivo for suportado pelo seu manipulador de coluna, atribua seu valor de dados a *pvarData* e retorne S \_ OK. Se o arquivo não tiver suporte do seu manipulador de coluna, retorne S \_ false sem atribuir um valor a *pvarData*.

Várias pastas conterão vários arquivos que não têm suporte em nenhum manipulador de coluna específico. Para melhorar a eficiência, [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) deve primeiro verificar o membro **pwszExt** da estrutura apontada por *pscd*. Esse membro contém a extensão de nome de arquivo. Se a extensão indicar que o arquivo não é um membro de um tipo de arquivo com suporte pelo seu manipulador, evite o processamento desnecessário retornando imediatamente S \_ false.

 

 
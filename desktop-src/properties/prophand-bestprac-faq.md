---
description: Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: Práticas recomendadas e perguntas frequentes do manipulador de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5188e66f08f3c6cf449f8bc61feb6aac829d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171591"
---
# <a name="property-handler-best-practices-and-faq"></a>Práticas recomendadas e perguntas frequentes do manipulador de propriedades

Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.

Este tópico é organizado da seguinte maneira:

-   [Práticas recomendadas](#property-handler-best-practices-and-faq)
    -   [Substituindo Propriedades do sistema de arquivos](#overriding-file-system-properties)
    -   [Armazenando Propriedades em formatos de arquivo baseados em XML](#storing-properties-in-xml-based-file-formats)
    -   [Propriedades computadas](#computed-properties)
-   [Perguntas frequentes](#property-handler-best-practices-and-faq)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices"></a>Práticas Recomendadas

As práticas recomendadas descritas aqui fornecem dicas úteis de implementação.

### <a name="overriding-file-system-properties"></a>Substituindo Propriedades do sistema de arquivos

Algumas propriedades de arquivos são fornecidas pela fonte de dados do sistema de arquivos, como:

-   \_Nome de arquivo PKEY
-   \_Extensão PKEY
-   PKEY \_ modifiedtime

Em geral, os manipuladores de propriedade não podem fornecer valores para essas propriedades. No entanto, em alguns casos, essas propriedades podem ser substituídas com base nas informações de registro fornecidas pelo manipulador de propriedade. Manipuladores de propriedade populam **\_ classes hKey \_ raiz** \\ **CLSID** \\ *{Handler CLSID}* \\ **OverrideFileSystemProperties** com os nomes das propriedades que desejam substituir. Isso é limitado a um conjunto fixo de propriedades mostrado na lista a seguir da qual o sistema tem conhecimento.

A substituição tem suporte para os seguintes valores de propriedade:

-   [Sistema. Kind](./props-system-kind.md)
-   [System. FileName](./props-system-filename.md)
-   [System. IsPinnedToNameSpaceTree](./props-system-ispinnedtonamespacetree.md)
-   [System.ItemNameDisplay](./props-system-itemnamedisplay.md)
-   [System. SFGAOFlags](./props-system-sfgaoflags.md)
-   [System. ItemPathDisplay](./props-system-itempathdisplay.md)
-   [System. ItemPathDisplayNarrow](./props-system-itempathdisplaynarrow.md)
-   [System. ItemFolderNameDisplay](./props-system-itemfoldernamedisplay.md)
-   [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)
-   [System. ItemFolderPathDisplayNarrow](./props-system-itemfolderpathdisplaynarrow.md)

Para obter uma lista completa de todas as propriedades do Shell, consulte [Propriedades do Shell](./props.md).

> [!IMPORTANT]
> Os valores de propriedade substituídos são usados somente quando os arquivos são indexados. Assim, a pesquisa de arquivos da fonte de dados do sistema de arquivos não revela os valores substituídos.

 

### <a name="storing-properties-in-xml-based-file-formats"></a>Armazenando Propriedades em formatos de arquivo baseados em XML

Há duas opções básicas disponíveis para armazenar propriedades em formatos de arquivo baseados em XML:

-   Armazene cada propriedade usando elementos XML e atributos de acordo com o esquema XML do documento. Essa abordagem é mais "amigável para XML".
-   Serialize todo o repositório de propriedades em um BLOB (objeto binário grande) de memória, converta o BLOB em uma cadeia de caracteres codificada em Base64 e, em seguida, armazene essa cadeia de caracteres no XML. Essa é a mais simples das duas abordagens e pode ser usada para fornecer suporte trivial aos metadados abertos.

Alguns manipuladores podem combinar essas abordagens, armazenando alguns valores importantes no formato XML padrão e armazenando o restante em um BLOB, por exemplo.

### <a name="computed-properties"></a>Propriedades computadas

Algumas propriedades são derivadas de atributos específicos de um arquivo. Por exemplo, a propriedade [System. Image. Dimensions](./props-system-image-dimensions.md) é determinada pelas dimensões reais da imagem em um arquivo de imagem. Como esses valores de propriedade não podem ser alterados pelo manipulador de propriedades, eles são marcados `isInnate="true"` na descrição da propriedade. Outras propriedades são computadas de uma parte de uma propriedade específica ou agregando os valores de várias propriedades. Como as atualizações dessas propriedades "computadas" poderiam criar ambiguidades quanto à forma como os valores de "origem" devem ser alterados, as propriedades computadas devem ser marcadas `isInnate="true"` na descrição da propriedade ou relatadas como somente leitura. A última opção está disponível instruindo o manipulador a retornar S \_ false de [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable).

## <a name="frequently-asked-questions"></a>Perguntas frequentes

Esta seção fornece respostas para perguntas frequentes sobre propriedades e manipuladores de propriedade e respostas de acompanhamento.

-   **Pergunta:** Por que o meu manipulador de propriedades não está sendo carregado pelo indexador do Windows Search?

    O indexador de pesquisa do Windows é executado como um serviço do sistema e não pode carregar DLLs armazenadas no diretório de perfil do usuário. Se você estiver criando e Depurando usando Microsoft Visual Studio, ele posicionará a DLL no seu perfil de usuário (e, portanto, não será carregado pelo indexador). Para solucionar esse erro, copie a DLL fora da sua pasta de perfil (por exemplo, em **C: \\ Program Files \\ nomedoseuaplicativo**) e registre-o lá.

    Para obter diretrizes mais específicas sobre como desenvolver manipuladores de propriedade para trabalhar com o indexador do Windows Search, consulte [desenvolvendo manipuladores de propriedade para o Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

-   **Pergunta:** Quais propriedades devem ser detectáveis por meio dos métodos de enumeração [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) ?

    Nem todos os clientes dos objetos de armazenamento de propriedade usam esses métodos. Alguns clientes estão cientes das propriedades que planejam solicitar diretamente (por nome de PKEY) ou recebem informações de propriedade por meio de uma lista de descrição de propriedade. Os métodos de descoberta de propriedade suportem vários outros cenários. Se uma propriedade não precisar participar desses cenários, ela não precisará ser enumerada. Portanto, um manipulador de propriedades pode produzir um valor não-VT \_ vazio para propriedades que não são descobertas por meio dos métodos [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) .

    No entanto, as propriedades devem ser visíveis por meio desses métodos se qualquer uma das seguintes condições forem atendidas:

    -   **Se a propriedade for indexada para que seja pesquisável:** Isso significa que ele está incluído no armazenamento de propriedades de pesquisa do Windows (indicado por `isColumn = "true"` no esquema de descrição da propriedade) ou disponível para pesquisas de texto completo ( `inInvertedIndex = "true"` ). Na ausência desses sinalizadores ou na ausência de uma descrição de propriedade, as propriedades do tipo "String" serão adicionadas automaticamente ao índice invertido para habilitar a pesquisa. Como a lista de propriedades conhecidas (aquelas com descrições de propriedade instaladas) no sistema de propriedades é muito grande (mais de 800 Propriedades), seria impraticável perguntar a cada manipulador de propriedade todas as propriedades registradas no sistema de propriedades. Em vez disso, o processo de indexação enumera as propriedades relevantes do manipulador de propriedade para cada item que indexa e usa os valores das propriedades enumeradas para criar o índice de texto completo.
    -   **Se a propriedade deve ser copiada quando o conjunto de propriedades do item for duplicado:** Para implementar uma função "copiar um conjunto de propriedades", o item de origem faz as propriedades que devem ser copiadas visíveis pelos métodos [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) . As propriedades que não precisam ser copiadas ou não fazem sentido ser copiada não devem ser incluídas.
    -   **Se o valor da propriedade não estiver vazio (VT \_ Empty):** os valores de propriedade vazios não serão úteis para os clientes. Quando os clientes tentam retornar valores de propriedade vazios, um valor de VT \_ vazio é retornado. Portanto, as propriedades com valores vazios não devem ser enumeradas.
    -   **Se a propriedade deve ser removida ao invocar a função "remover propriedades":** Este recurso existe para proteger a privacidade; Ele descobre todos os valores do manipulador de propriedade por meio da enumeração e Remove cada um selecionado para remoção pelo usuário.
        > [!Note]  
        > Enumerar Propriedades não comunica o conjunto de propriedades que um manipulador de propriedade específico suporta se o manipulador der suporte a um esquema fixo (e não a metadados abertos). Em vez disso, esses manipuladores devem documentar o conjunto de propriedades que eles suportam.

         

-   **Pergunta:** Como fazer saber quais formatos de arquivo dão suporte a metadados abertos?

    Para obter informações sobre o suporte para metadados abertos, consulte "tipos de arquivo que dão suporte a metadados abertos" em [tipos de arquivo](../shell/fa-file-types.md).

-   **Pergunta:** \_Os valores nulos de VT podem ser armazenados usando um manipulador de propriedades?

    Não. \_Os valores nulos de VT serão convertidos em VT \_ vazio em chamadas para [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)) e [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Pergunta:** Quais formatos de cadeia de caracteres de data têm suporte na função [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) ?

    Geralmente, as propriedades que representam os valores de data/hora devem ser representadas usando VT \_ FILETIME. No entanto, muitas fontes de dados fornecem essas informações em forma de cadeia de caracteres. A API auxiliar do [**PropVariantChangeType**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) dá suporte à coerção de alguns formatos de data de cadeia de caracteres em valores [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , conforme mostrado na tabela a seguir.

    

    | Formatar                  | Windows Vista, Windows XP e Microsoft Windows Desktop Search (WDS) | Windows 7 | Observações                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | aaaa/mm/dd: hh: mm: SS. uuu | Sim                                                                   | Sim       | HORÁRIO y = ano, m = mês, d = data, h = horas (relógio de 24 horas), m = minutos, s = segundos, u = microssegundos                                                                                                           |
    | aaaa-mm-ddThh: mm: ssZ    | Não                                                                    | Sim       | **Especificação de formato ISO8601** UTC (indicado pelo indicador de fuso horário ' Z '); y = ano, m = mês, d = data, h = horas (relógio de 24 horas), m = minutos, s = segundos; ' T' é um delimitador para a parte de tempo.<br/> |

    

     

-   **Pergunta:** É possível criar um manipulador de propriedades somente leitura?

    Sim. Algumas implementações do manipulador de propriedades não dão suporte à gravação de valores de propriedade. Esses manipuladores de propriedade devem retornar STGM \_ E \_ ACCESSDENIED em chamadas para **IInitializeXXX:: Initialize** que passem STGM \_ ReadWrite ou em qualquer chamada para [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

    Todos os manipuladores de propriedade abertos no \_ modo de leitura STGM devem retornar STGM \_ E \_ ACCESSDENIED em chamadas para [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)).

-   **Pergunta:** Um manipulador de propriedades pode tratar uma propriedade como somente leitura, mesmo que o esquema indique que a propriedade é gravável?

    Sim. No sistema de esquema, as propriedades são anotadas como somente leitura (incluindo aquelas com `isInnate = "true"` ) ou leitura/gravação. Os manipuladores de propriedade que não dão suporte à gravação de uma determinada propriedade que o esquema diz devem ser graváveis devem implementar [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) e retornar S \_ false em chamadas para [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) para essa propriedade. Isso indica que no contexto desse manipulador e esse arquivo, a propriedade não é gravável.

    > [!Note]  
    > A ação inversa não é possível. Não é possível habilitar um manipulador de propriedades para gravar uma propriedade marcada como somente leitura no esquema

     

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando nomes de tipos](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> </dl>

 

 

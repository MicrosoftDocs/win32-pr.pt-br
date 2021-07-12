---
description: O objeto de dados é central para todas as transferências de dados do Shell.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Objeto de dados do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a6c411310b6c9e9f28df4de048d3b6909c44b9
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581624"
---
# <a name="shell-data-object"></a>Objeto de dados do Shell

O objeto de dados é central para todas as transferências de dados do Shell. Trata-se principalmente de um contêiner para manter os dados transferidos. No entanto, o destino também pode se comunicar com o objeto de dados para facilitar alguns tipos especializados de transferência de dados do Shell, como movimentações otimizadas. Este tópico fornece uma discussão geral sobre como os objetos de dados do Shell funcionam, como eles são construídos por uma fonte e como eles são tratados por um destino. Para uma discussão detalhada sobre como usar objetos de dados para transferir diferentes tipos de dados do Shell, consulte Tratamento de cenários de transferência [de dados do Shell.](datascenarios.md)

-   [Como os objetos de dados funcionam](#how-data-objects-work)
    -   [Formatos da área de transferência](#clipboard-formats)
    -   [Estrutura FORMATETC](#formatetc-structure)
    -   [Estrutura STGMEDIUM](#stgmedium-structure)
-   [Como uma origem cria um objeto de dados](#how-a-source-creates-a-data-object)
    -   [Como adicionar um objeto de memória global a um objeto de dados](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implementando IDataObject](#implementing-idataobject)
    -   [Implementando IDropSource](#implementing-idropsource)
-   [Como um destino trata um objeto de dados](#how-a-target-handles-a-data-object)
    -   [Extraindo dados de shell de um objeto de dados](#extracting-shell-data-from-a-data-object)
    -   [Implementando IDropTarget](#implementing-idroptarget)
-   [Usando o objeto auxiliar do tipo "arrastar e soltar"](#using-the-drag-and-drop-helper-object)
    -   [Usando a interface IDragSourceHelper](#using-the-idragsourcehelper-interface)
    -   [Usando a interface IDropTargetHelper](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Como os objetos de dados funcionam

Os objetos de Component Object Model (COM) são criados pela fonte de dados para transferir dados para um destino. Normalmente, eles carregam mais de um item de dados. Há dois motivos para essa prática:

-   Embora quase qualquer tipo de dados possa ser transferido com um objeto de dados, a origem normalmente não sabe que tipo de dados o destino pode aceitar. Por exemplo, os dados podem ser uma parte de um documento de texto formatado. Embora o destino possa lidar com informações complexas de formatação, ele também pode aceitar apenas texto ANSI. Por esse motivo, os objetos de dados geralmente incluem os mesmos dados em vários formatos diferentes. Em seguida, o destino pode extrair os dados em um formato que ele pode manipular.
-   Os objetos de dados também podem conter itens de dados auxiliares que não são versões dos dados de origem. Esse tipo de item de dados normalmente fornece informações adicionais sobre a operação de transferência de dados. Por exemplo, o Shell usa itens de dados auxiliares para indicar se um arquivo deve ser copiado ou movido.

### <a name="clipboard-formats"></a>Formatos da área de transferência

Cada item de dados em um objeto de dados tem um formato associado, geralmente chamado de formato *de área de transferência*. Há vários formatos de área de transferência padrão, declarados em Winuser.h, que correspondem aos tipos de dados comumente usados. Os formatos da área de transferência são inteiros, mas normalmente são referenciados pelo nome equivalente, que tem o formato CF \_ *XXX.* Por exemplo, o formato da área de transferência para texto ANSI é CF \_ TEXT.

Os aplicativos podem estender o intervalo de formatos de área de transferência disponíveis definindo formatos privados. Para definir um formato privado, um aplicativo chama [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) com uma cadeia de caracteres que identifica o formato. O inteiro sem sinal que a função retorna é um valor de formato válido que pode ser usado como um formato de área de transferência padrão. No entanto, a origem e o destino devem registrar o formato para usá-lo. Com uma exceção,[CF \_ HDROP,](clipboard.md)os formatos de área de transferência usados para transferir dados do Shell são definidos como formatos privados. Eles devem ser registrados pela origem e pelo destino antes que possam ser usados. Para ver uma descrição dos formatos de área de transferência do Shell disponíveis, consulte Formatos da área de transferência do Shell.

Embora haja algumas exceções, os objetos de dados normalmente contêm apenas um item de dados para cada formato de área de transferência que eles suportam. Essa correlação um-para-um entre formato e dados permite que o valor de formato seja usado como um identificador para o item de dados associado. Na verdade, ao discutir o conteúdo de um objeto de dados, um item específico de dados normalmente é chamado de "formato" e é referenciado por seu nome de formato. Por exemplo, frases como "Extrair o formato CF \_ TEXT..." normalmente são usados ao discutir o item de dados de texto ANSI de um objeto de dados.

Quando o destino de soltar recebe o ponteiro para o objeto de dados, o destino de soltar enumera os formatos disponíveis para determinar quais tipos de dados estão disponíveis. Em seguida, ele solicita um ou mais dos formatos disponíveis e extrai os dados. A maneira específica de o destino extrair dados do Shell de um objeto de dados varia de acordo com o formato; isso é discutido em detalhes em [Como um destino trata um objeto de dados](#how-a-target-handles-a-data-object).

Com transferências de dados simples da área de transferência, os dados são colocados em um objeto de memória global. O endereço desse objeto é colocado na Área de Transferência, juntamente com seu formato. O formato da área de transferência informa ao destino que tipo de dados ele encontrará no endereço associado. Embora as transferências de área de transferência simples sejam fáceis de implementar:

-   Os objetos de dados fornecem uma maneira muito mais flexível de transferir dados.
-   Os objetos de dados são mais adequados para transferir grandes quantidades de dados.
-   Os objetos de dados devem ser usados para transferir dados com uma operação do tipo "arrastar e soltar".

Por esses motivos, todas as transferências de dados do Shell usam objetos de dados. Com objetos de dados, os formatos de área de transferência não são usados diretamente. Em vez disso, os itens de dados são identificados com uma generalização do formato da área de transferência, uma [**estrutura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc)

### <a name="formatetc-structure"></a>Estrutura FORMATETC

A [**estrutura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) é uma versão estendida de um formato de área de transferência. Conforme usado para transferências de dados do Shell, a **estrutura FORMATETC** tem as seguintes características:

-   Um item de dados ainda é identificado pelo formato da área de transferência, no **membro cfFormat.**
-   A transferência de dados não está limitada a objetos de memória global. O **membro tymed** é usado para indicar o mecanismo de transferência de dados contido na estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) associada. Ele é definido como um dos [**valores XXX do TYMED. \_**](/windows/win32/api/objidl/ne-objidl-tymed)
-   O Shell usa o **membro lIndex** com seu formato [CFSTR \_ FILECONTENTS](clipboard.md) para permitir que um objeto de dados contenha mais de um item de dados por formato. Para ver uma discussão sobre como usar esse formato, consulte a seção Using *the CFSTR \_ FILECONTENTS Format to Extract Data from a File* (Usando o formato FILECONTENTS CFSTR para extrair dados de um arquivo) em Tratamento de cenários de transferência de [dados do shell.](datascenarios.md)
-   O **membro dwAspect** normalmente é definido como DVASPECT \_ CONTENT. No entanto, há três valores definidos em Shlobj.h que podem ser usados para transferência de dados do Shell. 

    | Valor               | Descrição                                                                                       |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | DVASPECT \_ COPY      | Usado para indicar que o formato representa uma cópia dos dados.                                   |
    | LINK DE DVASPECT \_      | Usado para indicar que o formato representa um atalho para os dados.                               |
    | DVASPECT \_ SHORTNAME | Usado com o formato CF HDROP para solicitar um caminho de arquivo com os nomes abreviados \_ para o formato 8.3. |

    

     

-   O **membro ptd** não é usado para transferências de dados do Shell e normalmente é definido como **NULL.**

### <a name="stgmedium-structure"></a>Estrutura STGMEDIUM

A [**estrutura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) fornece acesso aos dados que estão sendo transferidos. Há suporte para três mecanismos de transferência de dados para dados do Shell:

-   Um objeto de memória global.
-   Uma interface [**IStream.**](/windows/win32/api/objidl/nn-objidl-istream)
-   Uma [**interface IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage)

O **membro tymed** da estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) é um [**valor XXX TYMED \_**](/windows/win32/api/objidl/ne-objidl-tymed) que identifica o mecanismo de transferência de dados. O segundo membro é um ponteiro usado pelo destino para extrair os dados. O ponteiro pode ser um de uma variedade de tipos, dependendo do **valor tymed.** Os três **valores marcados** que são usados para transferências de dados do Shell são resumidos na tabela a seguir, juntamente com seu nome de **membro STGMEDIUM** correspondente.



| Valor de tymed     | Nome do membro | Descrição                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **Hglobal** | Um ponteiro para um objeto de memória global. Esse tipo de ponteiro normalmente é usado para transferir pequenas quantidades de dados. Por exemplo, o Shell usa objetos de memória global para transferir cadeias de caracteres de texto curto, como nomes de arquivo ou URLs.                                                                                    |
| TYMED \_ ISTREAM  | **pstm**    | Um ponteiro para uma interface [**IStream.**](/windows/win32/api/objidl/nn-objidl-istream) Esse tipo de ponteiro é preferencial para a maioria das transferências de dados do Shell porque requer relativamente pouca memória em comparação com o \_ TYMED HGLOBAL. Além disso, o mecanismo de transferência de dados ISTREAM TYMED não exige que a origem armazene seus \_ dados de nenhuma maneira específica. |
| TYMED \_ ISTORAGE | **pstg**    | Um ponteiro para uma interface [**IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage) O destino chama os métodos de interface para extrair os dados. Assim como o TYMED \_ ISTREAM, esse tipo de ponteiro requer relativamente pouca memória. No entanto, como o ISTORAGE TYMED é menos flexível do que \_ o TYMED \_ ISTREAM, ele não é tão comumente usado.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>Como uma origem cria um objeto de dados

Quando um usuário inicia uma transferência de dados do Shell, a origem é responsável por criar um objeto de dados e carregá-lo com dados. O procedimento a seguir resume o processo:

1.  Chame [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obter um valor de formato de área de transferência válido para cada formato de Shell que será incluído no objeto de dados. Lembre-se [de que o CF \_ HDROP](clipboard.md) já é um formato de área de transferência válido e não precisa ser registrado.
2.  Para cada formato a ser transferido, coloque os dados associados em um objeto de memória global ou crie um objeto que fornece acesso a esses dados por meio de uma interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou [**IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage) As interfaces **IStream** **e IStorage** são criadas usando técnicas COM padrão. Para uma discussão sobre como manipular objetos de memória global, consulte [How to Add a Global Memory Object to a Data Object](#how-to-add-a-global-memory-object-to-a-data-object).
3.  Crie [**estruturas FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) [**e STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) para cada formato.
4.  Insinue um objeto de dados.
5.  Carregue os dados no objeto de dados chamando o método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para cada formato com suporte e passando as estruturas [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) do formato.
6.  Com transferências de dados da área de transferência, chame [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) para colocar um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados na Área de Transferência. Para transferências do arrastar e soltar, inicie um *loop de arrastar* chamando [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop) O **ponteiro IDataObject** será passado para o destino de soltar quando os dados são descartados, encerrando o loop de arrastar.

O objeto de dados agora está pronto para ser transferido para o destino. Para transferências de dados da área de transferência, o objeto é simplesmente mantido até que o destino o solicita chamando [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Para transferências de dados do tipo "arrastar e soltar", o objeto de dados é responsável por criar um ícone para representar os dados e movimentação conforme o usuário move o cursor. Enquanto o objeto está no loop de arrastar, a origem recebe informações de status por meio de sua interface [**IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Para mais discussão, consulte [Implementando IDropSource](#implementing-idropsource).

A origem não receberá nenhuma notificação se o objeto de dados for recuperado da Área de Transferência por um destino. Quando um objeto é descartado em um destino por uma operação do tipo "arrastar e soltar", a função [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) que foi chamada para iniciar o loop de arrastar retornará.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Como adicionar um objeto de memória global a um objeto de dados

Muitos dos formatos de dados do Shell estão na forma de um objeto de memória global. Use o procedimento a seguir para criar um formato que contém um objeto de memória global e carregá-lo no objeto de dados:

1.  Crie uma [**estrutura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) De definir **o membro cfFormat** como o valor de formato de área de transferência apropriado e o membro **tymed** como TYMED \_ HGLOBAL.
2.  Crie uma [**estrutura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) De definir **o membro tymed** como TYMED \_ HGLOBAL.
3.  Crie um objeto de memória global chamando [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) para alocar um bloco de memória de tamanho íntepar.
4.  Atribua o bloco de dados a ser transferido para o endereço retornado por [**GlobalAlloc.**](/windows/win32/api/winbase/nf-winbase-globalalloc)
5.  Atribua o endereço do objeto de memória global ao **membro hGlobal** da [**estrutura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)
6.  Carregue o formato no objeto de dados chamando [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) e passando as estruturas [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) criadas nas etapas anteriores.

A função de exemplo a seguir cria um objeto de memória global que contém um **valor DWORD** e o carrega em um objeto de dados. O **parâmetro pdtobj** é um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados, **cf** é o valor de formato da área de transferência e **dw** é o valor de dados.


```C++
STDAPI DataObj_SetDWORD(IDataObject *pdtobj, UINT cf, DWORD dw)
{
    FORMATETC fmte = {(CLIPFORMAT) cf, 
                      NULL, 
                      DVASPECT_CONTENT, 
                      -1, 
                      TYMED_HGLOBAL};
    STGMEDIUM medium;

    HRESULT hres = E_OUTOFMEMORY;
    DWORD *pdw = (DWORD *)GlobalAlloc(GPTR, sizeof(DWORD));
    
    if (pdw)
    {
        *pdw = dw;       
        medium.tymed = TYMED_HGLOBAL;
        medium.hGlobal = pdw;
        medium.pUnkForRelease = NULL;

        hres = pdtobj->SetData(&fmte, &medium, TRUE);
 
        if (FAILED(hres))
            GlobalFree((HGLOBAL)pdw);
    }
    return hres;
}
```



### <a name="implementing-idataobject"></a>Implementando IDataObject

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) é a interface primária de um objeto de dados. Ele deve ser implementado por todos os objetos de dados. Ele é usado pela origem e pelo destino para uma variedade de finalidades, incluindo:

-   Carregando dados no objeto de dados.
-   Extraindo dados do objeto de dados.
-   Determinando quais tipos de dados estão no objeto de dados.
-   Fornecer comentários ao objeto de dados sobre o resultado da transferência de dados.

[**IDataObject dá**](/windows/win32/api/objidl/nn-objidl-idataobject) suporte a vários métodos. Esta seção discute como implementar os três métodos mais importantes para objetos de dados do Shell, [SetData,](#setdata-method) [EnumFormatEtc](#enumformatetc-method)e [GetData.](#getdata-method) Para uma discussão sobre os outros métodos, consulte a **referência IDataObject.**

### <a name="setdata-method"></a>Método SetData

A função principal do método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) é permitir que a origem carregue dados no objeto de dados. Para cada formato a ser incluído, a origem cria uma estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para identificar o formato e uma [**estrutura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) para manter um ponteiro para os dados. Em seguida, a origem chama o método **IDataObject::SetData** do objeto e passa as estruturas **FORMATETC** e **STGMEDIUM do** formato. O método deve armazenar essas informações para que ela fique disponível quando o destino chamar [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extrair dados do objeto .

No entanto, ao transferir arquivos, o Shell geralmente coloca as informações para cada arquivo a ser transferido para um formato [ \_ CFSTR FILECONTENTS](clipboard.md) separado. Para distinguir os diferentes arquivos, o membro **lIndex** da estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) de cada arquivo é definido como um valor de índice que identifica o arquivo específico. Sua [**implementação de IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) deve ser capaz de armazenar vários formatos FILECONTENTS CFSTR que diferem apenas por seus \_ membros **lIndex.**

Enquanto o cursor está sobre a janela de destino, o destino pode usar o objeto auxiliar do tipo ["arrastar](#using-the-drag-and-drop-helper-object) e soltar" para especificar a imagem de arrastar. O objeto auxiliar do tipo "arrastar e soltar" chama [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para carregar formatos privados no objeto de dados usado para suporte entre processos. Para dar suporte ao objeto auxiliar do tipo "arrastar e soltar", a implementação **de IDataObject::SetData** deve ser capaz de aceitar e armazenar formatos privados arbitrários.

Depois que os dados são descartados, alguns tipos de transferência de dados do Shell exigem que o destino chame [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para fornecer ao objeto de dados informações sobre o resultado da operação de soltar. Por exemplo, ao mover arquivos com uma operação de movimentação otimizada, o destino normalmente exclui os arquivos originais, mas não é necessário fazer isso. O destino informa ao objeto de dados se ele excluiu os arquivos chamando **IDataObject::SetData** com um [formato \_ CFSTR LOGICALPERFORMEDDROPEFFECT.](clipboard.md) Há vários outros [formatos de área](clipboard.md) de transferência do Shell que também são usados pelo destino para passar informações para o objeto de dados. Sua **implementação de IDataObject::SetData** deve ser capaz de reconhecer esses formatos e responder adequadamente. Para mais discussão, consulte [Tratamento de cenários de transferência de dados de shell.](datascenarios.md)

### <a name="enumformatetc-method"></a>Método EnumFormatEtc

Quando o destino recebe um objeto de dados, ele normalmente chama [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para determinar quais formatos o objeto contém. O método cria um objeto de enumeração OLE e retorna um ponteiro para a interface [**IEnumFORMATETC do**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) objeto. Em seguida, o destino usa a interface para enumerar os formatos disponíveis.

Um objeto de enumeração sempre deve enumerar os formatos disponíveis em ordem de qualidade, começando com o melhor. A qualidade relativa dos formatos é definida pela fonte de soltar. Em geral, os formatos de mais alta qualidade contêm os dados mais completos e mais completos. Por exemplo, uma imagem de cor de 24 bits normalmente seria considerada uma qualidade mais alta do que uma versão em escala de cinza dessa imagem. O motivo para enumerar formatos em ordem de sua qualidade é que os destinos normalmente enumeram até chegar a um formato que eles suportam e, em seguida, usam esse formato para extrair os dados. Para que esse procedimento produza o melhor formato disponível que o destino pode dar suporte, os formatos devem ser enumerados em ordem de sua qualidade.

Um objeto de enumeração para dados do Shell é implementado da mesma maneira que para outros tipos de transferência de dados, com uma exceção notável. Como os objetos de dados normalmente contêm apenas um item de dados por formato, eles normalmente enumeram todos os formatos passados para [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). No entanto, conforme discutido na seção [método SetData,](#setdata-method) os objetos de dados do Shell podem conter vários [formatos \_ FILECONTENTS DO CFSTR.](clipboard.md)

Como a finalidade de [**IDataObject::EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) é permitir que o destino determine quais tipos de dados estão presentes, não é necessário enumerar mais de um formato [ \_ FILECONTENTS CFSTR.](clipboard.md) Se o destino precisar saber quantos desses formatos o objeto de dados contém, o destino poderá recuperar essas informações do formato DESCRIPTOR DO CFSTR QUE \_ acompanha. Para mais discussão sobre como implementar **IDataObject::EnumFormatEtc,** consulte a documentação de referência do método.

### <a name="getdata-method"></a>Método GetData

O destino chama [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para extrair um formato de dados específico. O destino especifica o formato passando a estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) apropriada. **IDataObject::GetData** retorna a estrutura [**STGMEDIUM do**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) formato.

O destino pode definir o membro **tymed** da estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para um valor específico TYMED XXX para especificar qual mecanismo de transferência de dados será usado para \_  extrair os dados. No entanto, o destino também pode fazer uma solicitação mais genérica e permitir que o objeto de dados decida. Para solicitar que o objeto de dados selecione o mecanismo de transferência de dados, o destino define todos os valores XXX do TYMED \_  com suporte. [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) seleciona um desses mecanismos de transferência de dados e retorna a estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) apropriada. Por exemplo, **tymed** normalmente é definido como TYMED \_ HGLOBAL \| TYMED \_ ISTREAM \| TYMED ISTORAGE para solicitar qualquer um dos três mecanismos de transferência de dados \_ do Shell.

> [!Note]  
> Como pode haver vários formatos [ \_ FILECONTENTS CFSTR,](clipboard.md) os membros **cfFormat** e **tymed** da estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) não são suficientes para indicar qual estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) deve retornar. Para o formato \_ FILECONTENTS CFSTR, **IDataObject::GetData** também deve examinar o membro **lIndex** da estrutura **FORMATETC** para retornar a estrutura **STGMEDIUM** correta.

 

O [formato CFSTR \_ INDRAGLOOP](clipboard.md) é colocado em objetos de dados para permitir que os destinos verifiquem o status do loop do tipo "arrastar e soltar", evitando a renderização intensiva de memória dos dados do objeto. Os dados do formato são um **valor DWORD** definido como um valor diferente de zero se o objeto de dados estiver dentro de um loop de arrastar. O valor dos dados do formato será definido como zero se os dados foram descartados. Se um destino solicitar esse formato e ele não tiver sido carregado pela origem, [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) deverá responder como se a origem tivesse carregado o formato com um valor zero.

Enquanto o cursor está sobre a janela de destino, o destino pode usar o objeto auxiliar do tipo ["arrastar](#using-the-drag-and-drop-helper-object) e soltar" para especificar a imagem de arrastar. O objeto auxiliar do tipo "arrastar e soltar" chama [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para carregar formatos privados no objeto de dados usado para suporte entre processos. Posteriormente, ele [**chama IDataObject::GetData para**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) recuperá-los. Para dar suporte ao objeto auxiliar do tipo "arrastar e soltar", a implementação do Objeto de Dados do Shell deve ser capaz de retornar formatos privados arbitrários quando eles são solicitados.

### <a name="implementing-idropsource"></a>Implementando IDropSource

A origem deve criar um objeto que expõe uma interface [**IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Essa interface permite que a  origem atualize a imagem de arrastar que indica a posição atual do cursor e forneça comentários ao sistema sobre como encerrar uma operação do tipo "arrastar e soltar". **IDropSource** tem dois métodos: [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) e [**QueryContinueDrag.**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag)

### <a name="givefeedback-method"></a>Método GiveFeedback

Enquanto estiver no loop de arrastar, uma origem de soltar é responsável por manter o controle da posição do cursor e exibir uma imagem de arrastar apropriada. No entanto, em alguns casos, talvez você queira alterar a aparência da imagem de arrastar quando ela estiver sobre a janela do destino de soltar.

Quando o cursor entra ou sai da janela de destino e enquanto ele está se movendo sobre a janela de destino, o sistema chama periodicamente a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do destino. O destino responde com um [**valor DROPEFFECT**](../com/dropeffect-constants.md) que é encaminhado para a origem por meio do [**método GiveFeedback.**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) Se apropriado, a origem pode modificar a aparência do cursor com base **no valor DROPEFFECT.** Para obter mais detalhes, consulte **as referências GiveFeedback** e [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

### <a name="querycontinuedrag-method"></a>Método QueryContinueDrag

Esse método será chamado se o botão do mouse ou o estado do teclado mudar enquanto o objeto de dados estiver no loop de arrastar. Ele notifica a origem se a tecla ESC foi pressionada e fornece o estado atual das teclas modificadora de teclado, como CTRL ou SHIFT. O valor de retorno do método [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) especifica uma das três ações:

-   S \_ OK. Continuar a operação de arrastar
-   ARRASTAR E \_ \_ SOLTAR. Solte os dados. Em seguida, o sistema chama o método [**IDropTarget::D rop do**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) destino.
-   DRAGDROP \_ S \_ CANCEL. Encente o loop de arrastar sem soltar os dados. Esse valor normalmente será retornado se a tecla ESCAPE tiver sido pressionada.

Para mais discussão, consulte [**as referências QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) e [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

## <a name="how-a-target-handles-a-data-object"></a>Como um destino trata um objeto de dados

O destino recebe um objeto de dados quando recupera o objeto de dados da Área de Transferência ou o faz ser descartado na janela de destino pelo usuário. O destino pode então extrair dados do objeto de dados. Se necessário, o destino também pode notificar o objeto de dados do resultado da operação. Antes de uma transferência de dados do Shell, um destino de soltar deve se preparar para a operação:

1.  O destino deve chamar [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) para obter um valor de formato de área de transferência válido para todos os formatos de Shell, além de [CF \_ HDROP](clipboard.md), que podem ser incluídos no objeto de dados. O CF HDROP já é um formato de área de transferência \_ válido e não precisa ser registrado.
2.  Para dar suporte a uma operação do tipo "arrastar e soltar", o destino deve implementar uma interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e registrar uma janela de destino. Para registrar uma janela de destino, o destino chama [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) e passa o handle da janela e o ponteiro da interface **IDropTarget.**

Para transferências de área de transferência, o destino não recebe nenhuma notificação de que um objeto de dados foi colocado na Área de Transferência. Normalmente, um aplicativo é notificado de que um objeto está na Área de Transferência por uma ação do usuário, como clicar no botão Colar na barra de ferramentas do aplicativo. Em seguida, o destino recupera o ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados da Área de Transferência chamando [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Para transferências de dados do tipo "arrastar e soltar", o sistema usa a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do destino para fornecer ao destino informações sobre o progresso da transferência de dados:

-   O sistema chama [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando o cursor entra na janela de destino.
-   O sistema chama periodicamente [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) à medida que o cursor passa pela janela de destino, para dar ao destino a posição atual do cursor.
-   O sistema chama [**IDropTarget::D ragLeave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) quando o cursor sai da janela de destino.
-   O sistema chama [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) quando o usuário descarta o objeto de dados na janela de destino.

Para ver uma discussão sobre como implementar esses métodos, consulte [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Quando os dados são descartados, [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) fornece ao destino um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados. Em seguida, o destino usa essa interface para extrair dados do objeto de dados.

### <a name="extracting-shell-data-from-a-data-object"></a>Extraindo dados de shell de um objeto de dados

Depois que um objeto de dados tiver sido descartado ou recuperado da Área de Transferência, o destino poderá extrair os dados necessários. A primeira etapa no processo de extração normalmente é enumerar os formatos contidos pelo objeto de dados:

-   Chame [**IDataObject::EnumFormatEtc.**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) O objeto de dados cria um objeto de enumeração OLE padrão e retorna um ponteiro para sua interface [**IEnumFORMATETC.**](/windows/win32/api/objidl/nn-objidl-ienumformatetc)
-   Use os [**métodos IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) para enumerar os formatos contidos pelo objeto de dados. Essa operação geralmente recupera uma [**estrutura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para cada formato que o objeto contém. No entanto, o objeto de enumeração normalmente retorna apenas uma única estrutura **FORMATETC** para o formato [ \_ FILECONTENTS CFSTR,](clipboard.md) independentemente de quantos desses formatos estão contidos pelo objeto de dados.
-   Selecione um ou mais formatos a serem extraídos e armazene suas [**estruturas FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc)

Para recuperar um formato específico, passe a estrutura [**FORMATETC associada**](/windows/win32/api/objidl/ns-objidl-formatetc) para [**IDataObject::GetData.**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) Esse método retorna uma [**estrutura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que fornece acesso aos dados. Para especificar um mecanismo de transferência de dados específico, de definir o valor **marcado** da estrutura **FORMATETC** para o valor XXX TYMED \_  correspondente. Para solicitar que o objeto de dados selecione um mecanismo de transferência de dados, o destino define os valores TYMED XXX para cada mecanismo de transferência de dados que \_  o destino pode manipular. O objeto de dados seleciona um desses mecanismos de transferência de dados e retorna a estrutura **STGMEDIUM** apropriada.

Para a maioria dos formatos, o destino pode recuperar os dados passando a estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) que recebeu quando enumerou os formatos disponíveis. Uma exceção a essa regra é [CFSTR \_ FILECONTENTS.](clipboard.md) Como um objeto de dados pode conter várias instâncias desse formato, a estrutura **FORMATETC** retornada pelo enumerador pode não corresponder ao formato específico que você deseja extrair. Além de especificar os **membros cfFormat** e **tymed,** você também deve definir o membro **lIndex** como o valor de índice do arquivo. Para mais discussão, consulte a seção *Using the CFSTR \_ FILECONTENTS Format to Extract Data from a File* (Usando o formato FILECONTENTS CFSTR para extrair dados de um arquivo) em [Tratamento de cenários de transferência](datascenarios.md) de dados do shell

O processo de extração de dados depende do tipo de ponteiro contido pela estrutura [**STGMEDIUM retornada.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Se a estrutura contiver um ponteiro para uma interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou [**IStorage,**](/windows/win32/api/objidl/nn-objidl-istorage) use os métodos de interface para extrair os dados. O processo de extração de dados de um objeto de memória global é discutido na próxima seção.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Extraindo um objeto de memória global de um objeto de dados

Muitos dos formatos de dados do Shell estão na forma de um objeto de memória global. Use o procedimento a seguir para extrair um formato que contém um objeto de memória global de um objeto de dados e atribuir seus dados a uma variável local:

1.  Crie uma [**estrutura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) De definir **o membro cfFormat** como o valor de formato de área de transferência apropriado e o membro **tymed** como TYMED \_ HGLOBAL.
2.  Crie uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) vazia.
3.  Chame [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)e passe ponteiros para as estruturas [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

    Quando [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) retornar, a estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) conterá um ponteiro para o objeto de memória global que contém os dados.

4.  Atribua os dados a uma variável local chamando [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) e passando o **membro hGlobal** da [**estrutura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)
5.  Chame [**GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) para liberar o bloqueio no objeto de memória global.
6.  Chame [**ReleaseStgMedium para**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) liberar o objeto de memória global.

> [!Note]  
> Você deve usar [**ReleaseStgMedium para**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) liberar o objeto de memória global, não [**GlobalFree.**](/windows/win32/api/winbase/nf-winbase-globalfree)

 

O exemplo a seguir mostra como extrair um **valor DWORD** armazenado como um objeto de memória global de um objeto de dados. O **parâmetro pdtobj** é um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados, **cf** é o formato da área de transferência que identifica os dados desejados e **pdwOut** é usado para retornar o valor de dados.


```C++
STDAPI DataObj_GetDWORD(IDataObject *pdtobj, UINT cf, DWORD *pdwOut)
{    STGMEDIUM medium;
   FORMATETC fmte = {(CLIPFORMAT) cf, NULL, DVASPECT_CONTENT, -1, 
       TYMED_HGLOBAL};
    HRESULT hres = pdtobj->GetData(&fmte, &medium);
    if (SUCCEEDED(hres))
   {
       DWORD *pdw = (DWORD *)GlobalLock(medium.hGlobal);
       if (pdw)
       {
           *pdwOut = *pdw;
           GlobalUnlock(medium.hGlobal);
       }
       else
       {
           hres = E_UNEXPECTED;
       }
       ReleaseStgMedium(&medium);
   }
   return hres;
}
```



### <a name="implementing-idroptarget"></a>Implementando IDropTarget

O sistema usa a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para se comunicar com o destino enquanto o cursor está sobre a janela de destino. As respostas do destino são encaminhadas para a origem por meio de sua interface [**IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Dependendo da resposta, a origem pode modificar o ícone que representa os dados. Se o destino de soltar precisar especificar o ícone de dados, ele poderá fazer isso criando um objeto auxiliar do [tipo "arrastar e soltar".](#using-the-drag-and-drop-helper-object)

Com operações convencionais do tipo "arrastar e soltar", o destino informa o objeto de dados do resultado da operação definindo o parâmetro *pdwEffect* de [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) como o valor [**DROPEFFECT**](../com/dropeffect-constants.md) apropriado. Com objetos de dados do Shell, o destino também pode precisar chamar [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Para ver uma discussão sobre como os destinos devem responder para diferentes cenários de transferência de dados, consulte Tratamento de cenários de [transferência de dados do Shell.](datascenarios.md)

As seções a seguir discutem brevemente como implementar os métodos [**IDropTarget::D ragEnter,**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)e [**IDropTarget::D rop.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) Para obter mais detalhes, consulte a documentação de referência.

### <a name="dragenter-method"></a>Método DragEnter

O sistema chama o método [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando o cursor entra na janela de destino. Seus parâmetros fornecem o destino com o local do cursor, o estado das teclas modificadoras de teclado, como a tecla CTRL, e um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados. O destino é responsável por usar essa interface para determinar se ela pode aceitar qualquer um dos formatos contidos no objeto de dados. Se puder, normalmente deixa o valor de *pdwEffect* inalterado. Se ele não puder aceitar nenhum dado do objeto de dados, ele definirá o parâmetro *pdwEffect* como DROPEFFECT \_ None. O sistema passa o valor desse parâmetro para a interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) do objeto de dados para permitir que ele exiba a imagem de arrastar apropriada.

Os destinos não devem usar o método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) para renderizar dados do Shell antes de serem descartados. A renderização total dos dados do objeto para cada ocorrência desse tipo pode causar a parada do cursor de arrasto. Para evitar esse problema, alguns objetos shell contêm um formato [CFSTR \_ INDRAGLOOP](clipboard.md) . Ao extrair esse formato, os destinos podem verificar o status do loop de arrastar enquanto evitam o processamento intensivo de memória dos dados do objeto. O valor de dados do formato é um **DWORD** que é definido como um valor diferente de zero se o objeto de dados estiver dentro de um loop de arrastar. O valor de dados do formato será definido como zero se os dados tiverem sido descartados.

Se o destino puder aceitar dados do objeto de dados, ele deverá examinar **grfKeyState** para determinar se as teclas modificadoras foram pressionadas para modificar o comportamento de remoção normal. Por exemplo, a operação padrão é normalmente uma movimentação, mas a remoção da tecla CTRL geralmente indica uma operação de cópia.

Enquanto o cursor está sobre a janela de destino, o destino pode usar o objeto auxiliar do tipo " [arrastar e soltar](#using-the-drag-and-drop-helper-object) " para substituir a imagem de arrastar do objeto de dados por sua própria. Nesse caso, [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) deve chamar [**IDropTargetHelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) para passar as informações contidas nos parâmetros *DragEnter* para o objeto auxiliar do tipo "arrastar e soltar".

### <a name="dragover-method"></a>Método DragOver

À medida que o cursor se move dentro da janela de destino, o sistema chama periodicamente o método [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) . Seus parâmetros fornecem o destino com o local do cursor e o estado das teclas modificadoras de teclado, como a tecla CTRL. **IDropTarget::D ragover** tem muito as mesmas responsabilidades que o [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), e as implementações são geralmente muito semelhantes.

Se o destino estiver usando o objeto auxiliar de arrastar e soltar, [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) deverá chamar [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) para encaminhar as informações contidas nos parâmetros *DragOver* para o objeto auxiliar do tipo "arrastar e soltar".

### <a name="drop-method"></a>Método Drop

O sistema chama o método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) para notificar o destino de que o usuário removeu os dados, normalmente liberando o botão do mouse. **IDropTarget::D ROP** tem os mesmos parâmetros que [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). O destino normalmente responde extraindo um ou mais formatos do objeto de dados. Quando terminar, o destino deve definir o parâmetro *pdwEffect* para um valor [**DROPEFFECT**](../com/dropeffect-constants.md) que indica o resultado da operação. Para alguns tipos de transferência de dados do Shell, o destino também deve chamar [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) para passar um formato com informações adicionais sobre o resultado da operação para o objeto de dados. Para obter uma discussão detalhada, consulte [manipulando cenários de transferência de dados do Shell](datascenarios.md).

Se o destino estiver usando o objeto auxiliar do tipo "arrastar e soltar", [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) deverá chamar [**IDropTargetHelper::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) para encaminhar as informações contidas nos parâmetros [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) para o objeto auxiliar do tipo "arrastar e soltar".

## <a name="using-the-drag-and-drop-helper-object"></a>Usando o objeto auxiliar do tipo "arrastar e soltar"

O objeto auxiliar do tipo "arrastar e soltar" (CLSID \_ DragDropHelper) é exportado pelo shell para permitir que os destinos especifiquem a imagem de arrastar enquanto ela está sobre a janela de destino. Para usar o objeto auxiliar do tipo "arrastar e soltar", crie um objeto de servidor em processo chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com um identificador de classe (CLSID) de CLSID \_ DragDropHelper. O objeto auxiliar do tipo "arrastar e soltar" expõe duas interfaces que são usadas da seguinte maneira:

-   A interface [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) permite que o destino drop especifique um ícone para representar o objeto de dados.
-   A interface [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permite que o destino drop informe o objeto auxiliar do tipo "arrastar e soltar" do local do cursor e mostre ou oculte o ícone de dados.

### <a name="using-the-idragsourcehelper-interface"></a>Usando a interface IDragSourceHelper

A interface [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) é exposta pelo objeto auxiliar do tipo "arrastar e soltar" para permitir que um destino de soltura forneça a imagem que será exibida enquanto o cursor estiver sobre a janela de destino. O **IDragSourceHelper** fornece duas maneiras alternativas de especificar o bitmap a ser usado como uma imagem de arrastar:

-   Os destinos de destino que têm uma janela podem registrar uma \_ mensagem de janela di GETDRAGIMAGE para ele inicializando o objeto auxiliar do tipo "arrastar e soltar" com [**IDragSourceHelper:: InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow). Quando o destino recebe uma mensagem de DI \_ GETDRAGIMAGE, o manipulador coloca as informações de bitmap de imagem de arrastar na estrutura [**SHDRAGIMAGE**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) que é passada como o valor de *lParam* da mensagem.
-   Os destinos de soltar sem janela especificam um bitmap quando inicializam o objeto auxiliar do tipo "arrastar e soltar" com [**IDragSourceHelper:: InitializeFromBitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap).

### <a name="using-the-idroptargethelper-interface"></a>Usando a interface IDropTargetHelper

Essa interface permite que o destino de soltura notifique o objeto auxiliar do tipo "arrastar e soltar" quando o cursor entra ou sai do destino. Enquanto o cursor está sobre a janela de destino, [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permite que o destino dê ao objeto auxiliar do tipo "arrastar e soltar" as informações que o destino recebe por meio de sua interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .

Quatro dos métodos [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) —[**IDropTargetHelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**IDropTargetHelper::D Ragleave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave), [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)e [**IDropTargetHelper::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop)— estão associados ao método [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do mesmo nome. Para usar o objeto auxiliar do tipo "arrastar e soltar", cada um dos métodos **IDropTarget** deve chamar o método **IDropTargetHelper** correspondente para encaminhar as informações para o objeto auxiliar do tipo "arrastar e soltar". O quinto método **IDropTargetHelper** , [**IDropTargetHelper:: show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show), notifica o objeto auxiliar de arrastar e soltar para mostrar ou ocultar a imagem de arrastar. Esse método é usado ao arrastar uma janela de destino em um modo de vídeo de intensidade de cor baixo. Ele permite que o destino oculte a imagem de arrastar enquanto está pintando a janela.

 

 

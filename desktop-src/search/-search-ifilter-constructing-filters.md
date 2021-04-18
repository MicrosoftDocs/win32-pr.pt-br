---
description: É importante entender a estrutura de DLL necessária de um manipulador de filtro (uma implementação da interface IFilter).
ms.assetid: a2b5a813-573a-44d3-8780-99603e3246c1
title: Implementando manipuladores de filtro no Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5f326440b31b62ff5697274962f4d4a2cfe7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791073"
---
# <a name="implementing-filter-handlers-in-windows-search"></a>Implementando manipuladores de filtro no Windows Search

É importante entender a estrutura de DLL necessária de um manipulador de filtro (uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

Este tópico é organizado da seguinte maneira:

- [Implementando e exportando os pontos de entrada da DLL](#implementing-and-exporting-the-dll-entry-points)
- [Implementando a classe IFilter e a fábrica de classes](#implementing-the-ifilter-class-and-class-factory)
- [Herdando as interfaces COM](#inheriting-the-com-interfaces)
- [Implementando os métodos de interface COM](#implementing-the-com-interface-methods)
  - [Métodos COM que não são implementados](#com-methods-that-are-not-implemented)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

## <a name="implementing-and-exporting-the-dll-entry-points"></a>Implementando e exportando os pontos de entrada da DLL

Cada DLL do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) (indicado por Ifilter.dll nesta seção) deve implementar e exportar os seguintes pontos de entrada. Esses pontos de entrada normalmente são exportados usando um arquivo de definição de módulo (. def) para a interface **IFilter** ou usando a palavra-chave **\_ \_ declspec (dllexport)** . O arquivo DLL pode ser registrado para estar em qualquer pasta, mas geralmente reside na pasta% SystemRoot% \\ System32.

Os pontos de entrada da DLL são listados e descritos na tabela a seguir.

| Nome da DLL                                                                                     | Descrição da DLL                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver)            | O ponto de entrada [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) registra a dll como um filtro no registro. Você registra a DLL executando o programa de regsvr32.exe com o nome de arquivo DLL da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) como um argumento: `regsvr32.exe %SystemRoot%\system32\Ifilter.dll`                                              |
| [Função DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) | O ponto de entrada da [função DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) remove a dll como um manipulador persistente no registro. Você cancela o registro da DLL executando o programa regsvr32.exe com o `/u` sinalizador: `regsvr32.exe /u %SystemRoot%\system32\Ifilter.dll`                                                                                    |
| [Função DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)   | O cliente de indexação de conteúdo chama o ponto de entrada da [função DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) , por meio de Component Object Model (com), para criar um objeto de fábrica de classe para a interface de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e obter um ponteiro para a interface de fábrica de classes desse objeto.                                               |
| [Função DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)     | O cliente de indexação de conteúdo chama o ponto de entrada da [função DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) , por meio de com, para determinar se é possível descarregar a DLL do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  . A interface **IFilter** é descarregada depois de não ser usada por um intervalo de tempo, conforme especificado pelo valor do registro FilterIdleTimeOut. |

## <a name="implementing-the-ifilter-class-and-class-factory"></a>Implementando a classe IFilter e a fábrica de classes

Pelo menos duas classes, como CFilter e CFilterCF, normalmente são implementadas por cada DLL do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . A classe CFilter produz o objeto de interface **IFilter** que implementa a funcionalidade de filtragem de conteúdo. Suas funções de membro implementam os métodos de interface da interface **IFilter** . Cada classe **IFilter** requer um identificador de classe exclusivo (CLSID), que o implementador de interface **IFilter** gera.

A classe CFilterCF produz o objeto Class-Factory para a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . A fábrica de classes é chamada por meio de sua interface de [interface IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , pelo ponto de entrada da [função DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) da dll. A classe CFilterCF cria o objeto CFilter e retorna um ponteiro para [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown). Em casos mais complexos, um **IFilter** pode implementar uma hierarquia de classe no lugar da única classe CFilter.

## <a name="inheriting-the-com-interfaces"></a>Herdando as interfaces COM

O Windows Search 3,0 e posterior requer que você use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pelos seguintes motivos:

- Para garantir o desempenho e a compatibilidade futura.
- Para ajudar a aumentar a segurança. Os IFilters implementados com [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) são mais seguros porque o contexto no qual a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é executada não precisa dos direitos para abrir arquivos no disco ou pela rede.
- Embora o Windows Search Use somente [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), a classe de interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) também pode herdar a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e/ou implementações de interface de [interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) para compatibilidade com versões anteriores.

Essas interfaces são declaradas em arquivos incluídos no \\ diretório Mssdk include e têm IIDs (identificadores de interface predefinidos). O cliente de indexação de conteúdo consulta a interface do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) por meio de [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para determinar quais dessas interfaces usar ao filtrar o conteúdo.

## <a name="implementing-the-com-interface-methods"></a>Implementando os métodos de interface COM

A interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) implementa os métodos [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a classe de interface **IFilter** e a fábrica de classe de interface **IFilter** . A tabela a seguir lista, em ordem vtable, as interfaces específicas da interface do **IFilter** e os métodos que a interface **IFilter** deve implementar. A interface **IFilter** deve implementar pelo menos [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), mas pode implementar interfaces derivadas de IPersist adicionais.

| Interface COM                                                                             | Método                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interface IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)   | CreateInstance, LockServer                                                                                                                                                                                                                                                     |
| [Interface IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)  | GetLicInfo, RequestLicKey, CreateInstanceLic                                                                                                                                                                                                                                   |
| [**Visio**](/windows/win32/api/filter/nn-filter-ifilter)                                                        | [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init), [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext), [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue), [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) |
| [Interface IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist)               | GetClassID                                                                                                                                                                                                                                                                     |
| [Interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)    | IsDirty, carregar, salvar, SaveCompleted, GetCurFile                                                                                                                                                                                                                                 |
| [Interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) | IsDirty, carregar, salvar, GetSizeMax                                                                                                                                                                                                                                                |
| [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)            | IsDirty, carregar, salvar, GetSizeMax                                                                                                                                                                                                                                                |

A página de referência para cada método especifica os parâmetros e o comportamento funcional para esse método. Cada página de referência também fornece os códigos de resultado a serem implementados para esse método. As páginas de referência para os métodos [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) fornecem os códigos específicos à interface [em recursos do \_ ITF](../com/codes-in-facility-itf.md) de resultados a serem implementados, e o cliente de indexação de conteúdo também pode lidar com qualquer um dos códigos de resultado genéricos, como o recurso de instalação \_ nula e do \_ Win32. Para obter mais informações, consulte [estrutura de códigos de erro com](../com/structure-of-com-error-codes.md).

### <a name="com-methods-that-are-not-implemented"></a>Métodos COM que não são implementados

A interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) deve implementar pelo menos [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), mas não precisa implementar interfaces derivadas IPersist adicionais.

O Windows Search não precisa implementar os métodos COM listados na tabela a seguir.

| Método que não é necessário                               | Description                       |
|-----------------------------------------------------------|-----------------------------------|
| IPersistStream:: IsDirty                                   | Os filtros devem retornar E \_ NOTIMPL. |
| IPersistStream:: Save                                      | Os filtros devem retornar E \_ NOTIMPL. |
| IPersistStream:: GetSizeMax                                | Os filtros devem retornar E \_ NOTIMPL. |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Os filtros devem retornar E \_ NOTIMPL. |

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[Noções básicas sobre manipuladores de filtro no Windows Search](-search-ifilter-about.md)

[Práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)

[Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)

[Manipuladores de filtro que acompanham o Windows](-search-ifilter-implementations.md)

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)

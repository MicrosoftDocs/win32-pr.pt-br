---
description: Seu manipulador de filtro deve ser registrado. Você também pode localizar um manipulador de filtro existente para uma determinada extensão de nome de arquivo por meio do registro ou usando a interface ILoadFilter.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Registrando manipuladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090079"
---
# <a name="registering-filter-handlers"></a>Registrando manipuladores de filtro

Seu manipulador de filtro deve ser registrado. Você também pode localizar um manipulador de filtro existente para uma determinada extensão de nome de arquivo por meio do registro ou usando a interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .

Este tópico é organizado da seguinte maneira:

- [Registrando manipuladores de filtros para o Windows Search](#registering-filter-handlers)
  - [Abordagem obsoleta para registrar manipuladores de filtros](#obsolete-approach-for-registering-filters-handlers)
- [Substituindo manipuladores de filtro existentes](#replacing-existing-filter-handlers)
- [Localizando um manipulador de filtro para uma determinada extensão de arquivo](#finding-a-filter-handler-for-a-given-file-extension)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

> [!NOTE]  
> Um manipulador de filtro é uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

## <a name="registering-filters-handlers-for-windows-search"></a>Registrando manipuladores de filtros para o Windows Search

Os GUIDs necessários para registrar um novo manipulador de protocolo ou para localizar um manipulador de protocolo existente são listados na tabela a seguir.

| GUID                                     | Definido pelo usuário ou aplicativo | Descrição                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| **89BCB740-6119-101A-BCB7-00DD010655AF** | Aplicativo                 | O GUID da interface do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é uma constante de chave do registro para todos os manipuladores de filtro. |
| **{PersistentHandlerGUID}**              | Usuário                        | Este é o GUID para o manipulador persistente.                                                              |
| **{FilterHandlerCLSID}**                 | Usuário                        | Esse é o identificador de classe (CLSID) para o manipulador de filtro.                                              |
| **{ApplicationGUID}**                    | Usuário                        | Esse é um GUID intermediário (agregado).                                                                |

Os manipuladores de filtro devem ser registrados \_ na \_ máquina local HKEY porque SearchFilterHost.exe está em execução na conta System e, portanto, não pode acessar as chaves do registro para HKEY \_ Current \_ User para o usuário conectado. Além disso, o grupo de usuários deve ter acesso de leitura e execução ao manipulador de filtro. dll em si porque SearchFilterHost.exe remove todos os direitos de administrador e permite somente direitos de não administrador. Como o local do projeto do Visual Studio padrão está no diretório do usuário atual e, portanto, não concede permissões de leitura ao grupo de usuários, você deve mover o. dll ou alterar as ACLs para permitir acesso SearchFilterHost.exe.

Ao registrar um novo manipulador de filtro, recomendamos que você use um nome descritivo, por exemplo, o IFilter HTML.

**Para registrar seu novo manipulador de filtro:**

1. Especifique a extensão e o GUID do manipulador persistente que usarão o manipulador de filtro:

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. Registre seu manipulador de filtro com as seguintes chaves e valores:

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a>Abordagem obsoleta para registrar manipuladores de filtros

Essa abordagem não é recomendada para uso. Os filtros podem ser registrados para um CLSID que representa uma classe COM (Component Object Model) e/ou para uma extensão de nome de arquivo. Você poderia registrar ambos os filtros se precisar registrar um manipulador de filtro para uma classe e um manipulador de filtro diferente para uma extensão de nome de arquivo dentro da classe. Observe que um manipulador de filtro registrado para uma extensão de nome de arquivo tem precedência sobre um manipulador de filtro para um CLSID.

Essas entradas são entradas de registro OLE padrão até e incluindo a entrada para o CLSID de classe **\\ {ApplicationGUID}**. A DLL sample.dll implementa o comportamento de objeto em execução para a classe. txt. Observe a entrada extra, PersistentHandler. Essa entrada especifica a classe responsável pelas solicitações de agente para os objetos persistentes da classe de exemplo. A entrada em **PersistentAddinsRegistered** identifica a implementação responsável pela interface chamada **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter). A classe implementando o **\_ IFilter de IID** tem entradas de registro OLE padrão. A DLL InprocServer32 é carregada por meio do mecanismo OLE padrão.

O Windows Search observa o modelo de threading especificado para o manipulador de filtro. Quando o modelo de threading é definido como **ambos**, o manipulador de filtro deve ser thread-safe; caso contrário, se não for thread-safe, especifique **Apartment**. Observe que os manipuladores de filtro sempre devem ser thread-safe.

As entradas de registro de exemplo a seguir são para um manipulador de filtro registrado para uma extensão de nome de arquivo e classe. **{PersistentHandlerGUID}** e **{FilterHandlerCLSID}** são usados como variáveis indicando valores que precisam ser especificados pelo criador do manipulador de filtro. Os valores são do tipo REG \_ sz.

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a>Substituindo manipuladores de filtro existentes

Recomendamos que você não substitua os manipuladores de filtro internos para tipos de arquivo comuns, como. txt,. doc,. html,. URL e assim por diante, pois isso pode ter efeitos indesejados em outros componentes do sistema. A indexação de corpos de mensagens de email depende dos manipuladores de filtro. txt,. html e. rtf, por exemplo.

Se um novo manipulador de filtro para um tipo de arquivo estiver sendo instalado como uma substituição para um registro de filtro existente, o instalador deverá salvar o registro atual e restaurá-lo se o novo manipulador de filtro for desinstalado. Não há nenhum mecanismo para encadear filtros. Portanto, o novo manipulador de filtro é responsável por replicar qualquer funcionalidade necessária do filtro antigo.

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a>Localizando um manipulador de filtro para uma determinada extensão de arquivo

Você pode usar a interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para localizar um manipulador de filtro para uma determinada extensão de nome de arquivo. As entradas de registro de exemplo a seguir ilustram como fazer isso para arquivos HTML. Neste exemplo, o manipulador de filtro para documentos HTML é nlhtml.dll. Os valores são do tipo REG \_ sz.

**Para localizar o manipulador de filtro para uma determinada extensão de nome de arquivo:**

1. Verifique se a extensão do tipo de arquivos filtrado tem um manipulador persistente registrado na entrada do registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Extension. Nesse caso, deixe que essa chave seja {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. Se não houver um manipulador persistente registrado para a extensão, localize o CLSID associado ao tipo de documento na entrada do registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Permita que essa chave seja {ApplicationGUID}. Em seguida, determine se um manipulador persistente está registrado para o CLSID: usando {ApplicationGUID} localize o manipulador persistente para a \\ entrada de classe de software do hKey \_ local \_ Machine \\ \\ classes \\ CLSID \\ {ApplicationGUID}. Permita que essa chave seja {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. Determine o GUID do manipulador persistente: usando {PersistentHandlerGUID} localize o GUID do manipulador persistente para o tipo de documento. O valor na entrada do registro HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF produz o GUID do manipulador persistente para esse tipo de documento. Permita que essa chave seja {FilterHandlerCLSID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determine o manipulador de filtro: usando {FilterHandlerCLSID} que foi determinado na etapa anterior, localize o manipulador de filtro na entrada \\ HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32. Neste exemplo, o nome do manipulador de filtro descritivo usado é o IFilter HTML.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para implementar a interface **IFilter** .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[Sobre manipuladores de filtro no Windows Search](-search-ifilter-about.md)

[Práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)

[Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)

[Manipuladores de filtro que acompanham o Windows](-search-ifilter-implementations.md)

[Implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md)

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)

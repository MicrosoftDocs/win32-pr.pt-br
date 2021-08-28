---
description: Interfaces (Windows Runtime C++)
ms.assetid: CB05B5F8-BE15-4BE0-A651-F6E8912D649D
title: Interfaces (Windows Runtime)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e813bce21e44a7fe7a3b5f2feffbc31b78a4f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884685"
---
# <a name="interfaces"></a>Interfaces

## <a name="in-this-section"></a>Nesta seção

| Interface | Descrição |
|-|-|
| [**IActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iactivatableclassregistration) | Permite obter as informações de registro para uma classe. |
| [**IActivationFactory**](/windows/win32/api/activation/nn-activation-iactivationfactory) | Permite que classes sejam ativadas pelo Windows Runtime . |
| [**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference) | Permite recuperar uma referência ágil para um objeto. |
| [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) | Habilita o registro de um manipulador de notificação de desligamento de apartamento. |
| [**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) | Representa o método que é chamado quando uma ação assíncrona é concluída. |
| [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) | Representa uma ação assíncrona. |
| [**IAsyncActionProgressHandler &lt; TProgress&gt;**](/previous-versions//br205782(v=vs.85)) | Representa o método que é chamado quando uma ação assíncrona relata o progresso. |
| [**IAsyncActionWithProgress &lt; TProgress&gt;**](/previous-versions//br205784(v=vs.85)) | Representa uma ação assíncrona que relata o progresso. |
| [**IAsyncActionWithProgressCompletedHandler &lt; TProgress&gt;**](/previous-versions//br205785(v=vs.85)) | Representa o método que é chamado quando uma ação assíncrona que relata o progresso é concluída. |
| [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) | Fornece suporte para operações assíncronas. |
| [**IAsyncOperation &lt; TResult&gt;**](/previous-versions//br205802(v=vs.85)) | Representa uma operação assíncrona que retorna um resultado. |
| [**IAsyncOperationCompletedHandler &lt; TResult&gt;**](/previous-versions//br205803(v=vs.85)) | Representa o método que é chamado quando uma operação assíncrona é concluída. |
| [**IAsyncOperationProgressHandler**](/previous-versions//br205805(v=vs.85)) | Representa o método que é chamado quando uma operação assíncrona relata o progresso. |
| [**IAsyncOperationWithProgress**](/previous-versions//br205807(v=vs.85)) | Representa uma operação assíncrona que retorna um resultado e relata o progresso. |
| [**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85)) | Representa o método que é chamado quando uma operação assíncrona que relata o progresso é concluída. |
| [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative) | Representa um quadro de dados de áudio. |
| [**IAudioFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenativefactory) | Cria instâncias de [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative). |
| [**IBuffer**](/previous-versions//hh438362(v=vs.85)) | Representa uma matriz de bytes. |
| [**IBufferByteAccess**](/previous-versions//hh846267(v=vs.85)) | Representa um buffer como uma matriz de bytes. |
| [**IClosable**](/windows/win32/api/windows.foundation/nn-windows-foundation-iclosable) | Define um método para recursos de versão alocado. |
| [**ICompositionDrawingSurfaceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) | Interface de interoperação nativa que permite desenhar em um objeto Surface usando um RECT para definir a área na qual desenhar. |
| [**ICompositionDrawingSurfaceInterop2**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2) | Uma interface de interoperação nativa que permite que você leia novamente o conteúdo de uma superfície de desenho de composição (ou superfície de desenho virtual de composição). |
| [**ICompositionGraphicsDeviceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiongraphicsdeviceinterop) | Uma interface de interoperação nativa que permite obter e definir o dispositivo de gráficos. |
| [**IContactManagerInterop**](/previous-versions//dn302109(v=vs.85)) | Habilita o acesso a métodos [**ContactManager**](/uwp/api/Windows.ApplicationModel.Contacts.ContactManager?view=winrt-19041) em um aplicativo que gerencia várias janelas. |
| [**ICoreApplication**](/previous-versions//hh438365(v=vs.85)) | Permite que os aplicativos manipulem alterações de estado, gerenciem o Windows e se integrem a uma variedade de estruturas de interface do usuário. |
| [**ICoreApplicationExit**](/previous-versions//hh438366(v=vs.85)) | fornece os meios para que os aplicativos da Windows Store parem de ser executados. |
| [**ICoreApplicationInitialization**](/previous-versions//hh438370(v=vs.85)) | Contém um método Run que é usado para iniciar o objeto Application a partir do ponto de entrada de um aplicativo. |
| [**ICoreApplicationView**](/previous-versions//hh438372(v=vs.85)) | Representa uma exibição de um aplicativo. |
| [**ICoreImmersiveApplication**](/previous-versions//hh438382(v=vs.85)) | Contém métodos para gerenciar modos de exibição em um aplicativo. |
| [**ICoreInputInterop**](/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop) | habilita uma fonte de entrada em um objeto [**CoreInput**](https://www.bing.com/search?q=**CoreInput**) do aplicativo de repositório de Windows. |
| [**ICoreWindowInterop**](/windows/desktop/api/corewindow/nn-corewindow-icorewindowinterop) | Permite que os aplicativos obtenham a janela handleof a janela ([**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041)) associada a essa interface. |
| [**IDllServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration) | Permite obter as informações de registro para um servidor em processo. |
| [**IErrorReportingSettings**](/previous-versions//br205818(v=vs.85)) | fornece integração de depurador para aplicativos Windows Runtime. |
| [**IEventHandler &lt; T&gt;**](/previous-versions//hh438385(v=vs.85)) | Representa o método que manipulará um evento que tem dados de evento do tipo **T**. |
| [**IExeServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration) | Permite obter as informações de registro para um servidor fora de processo. |
| [**IExeServerRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserverregistration) | Representa um servidor de fora de processo registrado. |
| [**IFindReferenceTargetsCallback**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback) | Define a interface para retornos de chamada de [**IReferenceTracker:: FindTrackerTargets**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets). A implementação dessa interface deve passar quaisquer instâncias [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) encontradas para o método **FoundTrackerTarget** . |
| [**IInputPaneInterop**](/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop) | Habilita o acesso aos membros da classe [**InputPane**](/uwp/api/Windows.UI.ViewManagement.InputPane?view=winrt-19041) em um aplicativo de área de trabalho. |
| [**IInputStream**](/previous-versions//hh438387(v=vs.85)) | Permite obter uma operação de leitor assíncrona em um fluxo sequencial de bytes. |
| [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) | fornece a funcionalidade necessária para todas as classes de Windows Runtime. |
| [**IIterable &lt; T&gt;**](/previous-versions//br205825(v=vs.85)) | Expõe o iterador, que dá suporte à iteração simples em uma coleção de um tipo especificado. |
| [**IIterator &lt; T&gt;**](/previous-versions//br205827(v=vs.85)) | Dá suporte à iteração em uma coleção. |
| [**IKeyValuePair<K, V>**](/previous-versions//br205831(v=vs.85)) | Representa um par chave-valor. |
| [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo) | Permite recuperar o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) armazenado nas informações de erro com a chamada para RoOriginateLanguageException. |
| [**ILanguageExceptionErrorInfo2**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2) | Habilita projeções de linguagem para fornecer e recuperar informações de erro como com o [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo), com o benefício adicional de trabalhar entre limites de idioma. |
| [**ILanguageExceptionTransform**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform) | Permite que as projeções de linguagem tornem-se disponíveis para o sistema qualquer e todo o contexto de uma exceção que é gerada a partir do contexto de um manipulador catch que captura uma exceção diferente. |
| [**ILanguageExceptionStackBackTrace**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace) | Permite que as projeções forneçam rastreamento de pilha personalizado para essa exceção. |
| [**IMap<K, V>**](/previous-versions//br205834(v=vs.85)) | Representa uma coleção associativa. |
| [**IMapChangedEventArgs &lt; K&gt;**](/previous-versions//br205835(v=vs.85)) | Fornece dados para um [**evento MapChanged.**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) |
| [**IMapView<K, V>**](/previous-versions//br205838(v=vs.85)) | Representa uma exibição imutável em [**um IMap(K,V).**](/previous-versions//br205834(v=vs.85)) |
| [**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85)) | Fornece acesso a [**um IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) como uma matriz de bytes. |
| [**IMetaDataAssemblyImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport) | Fornece métodos para acessar e examinar o conteúdo de um manifesto do assembly. |
| [**Imetadatadispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) | Fornece métodos para criar um novo escopo de metadados ou abrir um existente. |
| [**Imetadatadispenserex**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenserex) | Estende a interface [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) para fornecer a capacidade de controlar como as APIs de metadados operam no escopo de metadados atual. |
| [**Imetadataimport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) | Fornece métodos para importar e manipular metadados existentes de um arquivo PE (executável portátil) ou de outra fonte, como uma biblioteca de tipos ou um binário de metadados de tempo de execução autônomo. |
| [**IMetaDataImport2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport2) | Estende a interface [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) para fornecer a capacidade de trabalhar com tipos genéricos. |
| [**Imetadatatables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) | Fornece métodos para armazenamento e recuperação de informações de metadados em tabelas. |
| [**IMetaDataTables2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables2) | Estende [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) para incluir métodos para trabalhar com fluxos de metadados. |
| [**IObservableMap<K, V>**](/previous-versions//br205851(v=vs.85)) | Notifica manipuladores de eventos de alterações dinâmicas em um mapa, como quando itens são adicionados ou removidos. |
| [**IObservableVector &lt; T&gt;**](/previous-versions//br205854(v=vs.85)) | Notifica manipuladores de eventos de alterações no vetor. |
| [**IOplockBreakingHandler**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-ioplockbreakinghandler) | Essa interface não está implementada no momento. |
| [**IOutputStream**](/previous-versions//hh438390(v=vs.85)) | Habilita a obtenção de uma operação de writer assíncrona em um fluxo sequencial de bytes. |
| [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) | Representa uma API de alto desempenho para exibir uma única página de um arquivo PDF (Formato de Documento Portátil). |
| [**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85)) | Habilita o controle dos desenvolvedores do depurador sobre o ciclo de vida de um aplicativo Windows Store, como quando ele é suspenso ou retomado. |
| [**IPlayToManagerInterop**](/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop) | Habilita o acesso [**aos métodos PlayToManager**](/uwp/api/Windows.Media.PlayTo.PlayToManager?view=winrt-19041) em um aplicativo Windows Store que gerencia várias janelas. |
| [**IPrintManagerInterop**](/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop) | Habilita o acesso [**aos métodos PrintManager**](/uwp/api/Windows.Graphics.Printing.PrintManager?view=winrt-19041) em um aplicativo Windows Store que gerencia várias janelas. |
| [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) | Representa um valor em um Windows de propriedades runtime. |
| [**IPropertyValueStatics**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics) | Cria [**objetos IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) que você pode armazenar em um armazenamento de propriedades. |
| [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) | Permite obter um leitor de byte assíncrono ou um autor de byte posicionado no local especificado em um fluxo de byte de acesso aleatório. |
| [**IRandomAccessStreamFileAccessMode**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-irandomaccessstreamfileaccessmode) | Fornece acesso ao modo de acesso ao arquivo que foi usado [**quando o método StorageFile.OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) foi chamado para abrir o fluxo de byte de acesso aleatório. |
| [**IReference &lt; T&gt;**](/previous-versions//br224583(v=vs.85)) | Permite estender o sistema de propriedades Windows Runtime para enumerações, estruturas e tipos delegados definidos pelo usuário. |
| [**IReferenceArray &lt; T&gt;**](/previous-versions//br224584(v=vs.85)) | Permite estender o sistema de Windows runtime para matrizes de enumerações, estruturas e tipos delegados definidos pelo usuário. |
| [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) | Define a interface implementada pela estrutura XAML para gerenciar referências de objeto XAML. |
| [**IReferenceTrackerHost**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost) | Define uma interface que fornece os serviços globais usados pelo sistema de coleta de lixo (GC) usado pela estrutura XAML. |
| [**IReferenceTrackerManager**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager) | Define a interface para um gerenciador de referência de objeto XAML. Implemente essa interface para gerenciar instâncias [**de IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) em objetos XAML. |
| [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) | Define uma interface implementada por um objeto do coletor de lixo referenciado de XAML. |
| [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) | Representa os detalhes de um erro, incluindo informações de erro restritas. |
| [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) | Representa um bitmap de software. |
| [**ISoftwareBitmapNativeFactory**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory) | Cria instâncias de [**ISoftwareBitmapNative.**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) |
| [**IStorageFolderHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istoragefolderhandleaccess) | Fornece acesso ao alça do sistema operacional de uma pasta de armazenamento. |
| [**IStorageItemHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istorageitemhandleaccess) | Fornece acesso ao alça do sistema operacional de um arquivo de armazenamento. |
| [**IStringable**](/windows/win32/api/windows.foundation/nn-windows-foundation-istringable) | Fornece uma maneira de representar o objeto atual como uma cadeia de caracteres. |
| [**ISurfaceImageSourceManagerNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative) | Permite executar operações em massa em todos os [**objetos SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) criados no mesmo processo. |
| [**ISurfaceImageSourceNativeWithD2D**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d) | Fornece a implementação de uma superfície compartilhada do Microsoft DirectX que é exibida em [**um SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) ou [**VirtualSurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.VirtualSurfaceImageSource?view=winrt-19041). |
| [**ISurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative) | Fornece a implementação de uma superfície de tamanho fixo compartilhada para Direct2D desenho. |
| [**ISuspendingDeferral**](isuspendingdeferral.md) | Gerencia uma operação de suspensão de aplicativo atrasada. |
| [**ISuspendingEventArgs**](isuspendingeventargs.md) | Fornece dados para um evento de suspensão de aplicativo. |
| [**ISuspendingOperation**](isuspendingoperation.md) | Fornece informações sobre uma operação de suspensão de aplicativo. |
| [**ISwapChainBackgroundPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative) | Fornece interoperação entre XAML e uma cadeia de permuta do DirectX. |
| [**ISwapChainPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative) | Fornece interoperação entre XAML e uma cadeia de permuta do DirectX. Ao contrário de [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), um **SwapChainPanel** pode aparecer em qualquer nível na árvore de exibição XAML e mais de 1 pode estar presente em qualquer árvore determinada. |
| [**ISwapChainPanelNative2**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2) | Fornece interoperação entre XAML e uma cadeia de permuta do DirectX. Ao contrário de [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), um **SwapChainPanel** pode aparecer em qualquer nível na árvore de exibição XAML e mais de 1 pode estar presente em qualquer árvore determinada. |
| [**ITypedEventHandler<TSender, TArgs>**](/previous-versions//hh438424(v=vs.85)) | Representa o método que manipulará um evento de um remetente do tipo **TSender** e dados de evento do tipo **T**. |
| [**IUnbufferedFileHandleOplockCallback**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback) | Define um método de retorno de chamada que você deseja executar quando o bloqueio oportunista para um handle que você recebe chamando o método [**IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle**](/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle) é desfeito. |
| [**IUnbufferedFileHandleProvider**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleprovider) | Fornece acesso a alças de um fluxo de byte de acesso aleatório criado pelo [**método StorageFile.OpenAsync.**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) |
| [**IVector &lt; T&gt;**](/previous-versions//br224590(v=vs.85)) | Representa uma coleção de elementos de acesso aleatório. |
| [**IVectorChangedEventArgs**](ivectorchangedeventargs.md) | Fornece dados para um [**evento VectorChanged.**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) |
| [**IVectorView &lt; T&gt;**](/previous-versions//br224594(v=vs.85)) | Representa uma exibição imutável em [**um IVector(T)**](/uwp/api/windows.foundation.collections.ivector-1?view=winrt-19041). |
| [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) | Representa um quadro de dados de vídeo. |
| [**IVideoFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenativefactory) | Cria instâncias de [**IVideoFrameNative.**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) |
| [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) | Representa uma exibição em um aplicativo. |
| [**IViewProviderFactory**](/previous-versions//hh438427(v=vs.85)) | Cria uma instância de exibições que implementam a interface [**IViewProvider.**](/previous-versions//hh438426(v=vs.85)) |
| [**IVirtualSurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) | Fornece a implementação de uma superfície compartilhada grande (maior que o tamanho da tela) para desenho do DirectX. |
| [**IVirtualSurfaceUpdatesCallbackNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative) | Fornece uma interface para a implementação de comportamentos de desenho quando [**um VirtualSurfaceImageSource**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) solicita uma atualização. |
| [**IWeakReference**](/windows/win32/api/weakreference/nn-weakreference-iweakreference) | Representa uma referência fraca a um objeto . |
| [**IWeakReferenceSource**](/windows/win32/api/weakreference/nn-weakreference-iweakreferencesource) | Representa um objeto de origem para o qual uma referência fraca pode ser recuperada. |
| [**MapChangedEventHandler<K, V>**](/previous-versions//br224612(v=vs.85)) | Representa o método que trata o [**evento MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) de um mapa observável. |
| [**VectorChangedEventHandler &lt; T&gt;**](/previous-versions//br224626(v=vs.85)) | Representa o método que trata o evento [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) de um vetor observável. |

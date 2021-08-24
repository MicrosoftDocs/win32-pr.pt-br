---
description: Uma referência para Windows funções C++ do Runtime.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: Funções (Windows Runtime)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: fbf0d4ce350251e1c13d1f6a3ff03c95068558098eac722979bc77499a094c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795006"
---
# <a name="functions-windows-runtime-c-reference"></a>Funções (Windows referência C++ do Runtime)

## <a name="in-this-section"></a>Nesta seção



| Função | Descrição |
|-|-|
| [**CoDecodeProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Localiza a implementação de uma interface COMPONENT OBJECT MODEL (COM) em um processo de servidor dado uma interface para um objeto com proxy. |
| [**CreateControlInput**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Cria um [**objeto ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) no thread de interface do usuário do chamador. |
| [**CreateControlInputEx**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Cria um [**objeto ICoreInputSourceBase em**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) um thread de trabalho ou no thread da interface do usuário.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Cria uma instância de IDirect3DDevice de um IDXGIDevice. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Cria uma instância de IDirect3DSurface de um IDXGISurface. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Cria uma instância de [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) de [um IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice). |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Cria uma instância de [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) de [um IDXGISurface.](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) |
| [**CreateRandomAccessStreamOnFile**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | Cria um Windows fluxo de acesso aleatório do Runtime para um arquivo. |
| [**CreateRandomAccessStreamOverStream**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | Cria um fluxo Windows de acesso aleatório do Runtime em torno de uma implementação base [**do IStream.**](/windows/win32/api/objidl/nn-objidl-istream) |
| [**CreateStreamOverRandomAccessStream**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | Cria um [**IStream em**](/windows/win32/api/objidl/nn-objidl-istream) torno de um Windows [**runtime IRandomAccessStream.**](/previous-versions//hh438400(v=vs.85)) |
| [**CreateXamlUIPresenter**](createxamluipresenter.md) | Uma função de criador estático que pode criar um [**XamlUIPresenter para**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) uma superfície de renderização em um aplicativo da área de trabalho. |
| [**DbgRaiseAssertionFailure**](/previous-versions//jj635749(v=vs.85)) | Gera uma declaração para depuração.  |
| [**GetDXGIInterface(IDirect3DDevice^, DXGI_TYPE**)**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Recupera uma interface DXGI de uma [instância IDirect3DDevice.](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) |
| [**GetDXGIInterface(IDirect3DSurface^, DXGI_TYPE**)**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Recupera uma interface DXGI de uma [instância IDirect3DSurface.](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) |
| [**GetDXGIInterfaceFromObject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Recupera uma interface DXGI de um objeto . |
| [**GetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Obtém o objeto de informações de erro restrito definido por uma chamada anterior para [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) no thread lógico atual. |
| [**HSTRING \_ UserFree**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Libera recursos no lado do servidor quando chamado por arquivos stub RPC. |
| [**HSTRING \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Libera recursos no lado do servidor quando chamado por arquivos stub RPC.  |
| [**HSTRING \_ UserMarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Marshaling de [**um objeto HSTRING**](hstring.md) no buffer RPC. |
| [**HSTRING \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Marshaling de [**um objeto HSTRING**](hstring.md) no buffer RPC. |
| [**HSTRING \_ UserSize**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Calcula o tamanho da transmissão do [**objeto HSTRING**](hstring.md) e obtém seu identificador e dados. |
| [**Usuário \_ HSTRINGSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Calcula o tamanho da transmissão do [**objeto HSTRING**](hstring.md) e obtém seu identificador e dados. |
| [**HSTRING \_ UserUnmarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Desmarca um [**objeto HSTRING**](hstring.md) do buffer RPC. |
| [**HSTRING \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Desmarca um [**objeto HSTRING**](hstring.md) do buffer RPC. |
| [**IsErrorPropagationEnabled**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | Indica se o [**evento CoreApplication.UnhandledErrorDetected**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) ocorre para os erros retornados pelo delegado registrado como uma função de retorno de chamada para um evento de API do runtime do Windows ou a conclusão de um método assíncrono. |
| [**DllGetActivationFactory**](/previous-versions//br205771(v=vs.85)) | Recupera a fábrica de ativação de uma DLL que contém classes ativas Windows Runtime. |
| [**MetaDataGetDispenser**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Cria uma classe de distribuidor. |
| [**PdfCreateRenderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Obtém uma instância da interface [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) para exibir uma única página de um arquivo PDF (Formato de Documento Portátil). |
| [**PdfRenderParams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Popula um [**stucture \_ \_ PARAMS**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) DE RENDERIZAÇÃO DE PDF. Uma estrutura PARAMS RENDER DE PDF representa um conjunto de propriedades para a saída de \_ uma única página de um arquivo \_ PDF. |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | Ativa a classe Windows Runtime especificada. |
| [**RoCaptureErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Salva o contexto de erro atual para que ele seja disponibilizado para chamadas posteriores para a [**função RoFailFastWithErrorContext.**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) |
| [**RoClearError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Remove as informações de erro existentes do TEB (bloco de ambiente de thread) atual. |
| [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Gera uma exceção não continuavel no processo atual. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Gera uma exceção não continuavel no processo atual e também permite incluir contexto de erro adicional que ainda não foi capturado pelo sistema operacional. |
| [**RoFreeParameterizedTypeExtra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Libera o handle alocado por [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid). |
| [**RoGetActivatableClassRegistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Habilita a recuperação de informações de registro de classe. |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Obtém a fábrica de ativação para a classe de runtime especificada. |
| [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Cria uma referência ágil para um objeto especificado pela interface especificada. |
| [**RoGetApartmentIdentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Obtém um identificador exclusivo para o apartment atual. |
| [**RoGetBufferMarshaler**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Fornece um marshaler IBuffer padrão para implementar a semântica associada à interface IBuffer quando ela é marshaled. |
| [**RoGetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | Obtém o comportamento de relatório atual Windows funções de erro do Runtime. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Localiza e recupera o arquivo de metadados que descreve a ABI (Interface Binária de Aplicativo) para o typename especificado. |
| [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Calcula o IID (identificador de interface) da interface ou do tipo delegado que resulta quando uma interface com parâmetros ou delegado é instanida com os argumentos de tipo especificados. |
| [**RoGetServerActivatableClasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Recupera as classes ativas que são registradas para um determinado servidor executável (EXE), que foi registrado na ID do pacote do processo de chamada. |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | Inicializa o runtime Windows no thread atual com o modelo de simultrreidade especificado. |
| [**RoInspectThreadErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Obtém o objeto de erro que representa a pilha de chamada no ponto em que o erro foi originado |
| [**RoInspectCapturedStackBackTrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Fornece uma maneira de para os depurador inspecionarem uma pilha de chamada de um processo de destino. |
| [**RoOriginateError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Relata um erro e uma cadeia de caracteres informativa para um depurador anexado. |
| [**RoOriginateErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Relata um erro e uma cadeia de caracteres informativa para um depurador anexado. |
| [**RoOriginateLanguageException**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Relata um erro, uma cadeia de caracteres informativa e um objeto de erro para um depurador anexado. |
| [**RoParameterizedTypeExtraGetTypeSignature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Obtém a assinatura de tipo usada para calcular o IID da última chamada para [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) com o identificador especificado. |
| [**RoParseTypeName**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Analisar um nome de tipo e parâmetros de tipo existentes, no caso de tipos parametrizados. |
| [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | Registra uma matriz de fábricas de ativação fora do processo para um Windows runtime exe. |
| [**RoRegisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Registra um retorno [**de chamada IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) a ser invocado quando o apartment atual é desligado. |
| [**RoReportUnhandledError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Dispara o Manipulador de Erros Global quando ocorre uma exceção sem-correção. |
| [**RoReportFailedDelegate**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Dispara o Manipulador de Erros Global quando ocorre uma falha de delegado. |
| [**RoResolveNamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | Determine os filhos diretos, tipos e sub-namespaces do namespace Windows Runtime especificado, de qualquer linguagem de programação com suporte no runtime Windows. |
| [**RoResolveRestrictedErrorInfoReference**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Retorna o ponteiro da interface [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) com base na referência determinada. |
| [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | Remove uma matriz de fábricas de ativação registradas do runtime Windows. |
| [**RoSetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | Define o comportamento de relatório de Windows funções de erro de Runtime. |
| [**RoTransformError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Relata um erro modificado e uma cadeia de caracteres informativa para um depurador anexado. |
| [**RoTransformErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Relata um erro transformado e uma cadeia de caracteres informativa para um depurador anexado. |
| [**RoUninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | Fecha o Windows Runtime no thread atual. |
| [**RoUnregisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Registra uma interface [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) registrada anteriormente. |
| [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Define o objeto de informações de erro restrito para o thread atual. |
| [**WindowsCompareStringOrdinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Compara dois objetos [**HSTRING especificados**](hstring.md) e retorna um inteiro que indica sua posição relativa em uma ordem de classificação. |
| [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Concatena duas cadeias de caracteres especificadas. |
| [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Cria um novo [**HSTRING com base**](hstring.md) na cadeia de caracteres de origem especificada. |
| [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Cria uma nova referência de cadeia de caracteres com base na cadeia de caracteres especificada. |
| [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Diminui a contagem de referência de um buffer de cadeia de caracteres. |
| [**WindowsDeleteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Descarta um buffer de cadeia de caracteres pré-alocado se ele não foi promovido para um [**HSTRING.**](hstring.md) |
| [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Cria uma cópia da cadeia de caracteres especificada. |
| [**WindowsGetStringLen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Obtém o comprimento, em caracteres Unicode, da cadeia de caracteres especificada. |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Obtém o buffer de backing para a cadeia de caracteres especificada. |
| [**WindowsInspectString**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | Fornece uma maneira de para os depurador exibirem o valor de um [**Windows Runtime HSTRING**](hstring.md) em outro espaço de endereço, remotamente ou de um despejo.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | Fornece uma maneira de para os depurador exibirem o valor de um [**Windows Runtime HSTRING**](hstring.md) em outro espaço de endereço, remotamente ou de um despejo.  |
| [**WindowsIsStringEmpty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Indica se a cadeia de caracteres especificada é a cadeia de caracteres vazia. |
| [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Aloca um buffer de caractere mutável para uso na [**criação de HSTRING.**](hstring.md) |
| [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Cria um [**HSTRING**](hstring.md) do [**BUFFER HSTRING \_ especificado.**](hstring-buffer.md) |
| [**WindowsReplaceString**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Substitui todas as ocorrências de um conjunto de caracteres na cadeia de caracteres especificada por outro conjunto de caracteres para criar uma nova cadeia de caracteres. |
| [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Indica se a cadeia de caracteres especificada tem caracteres nulos inseridos. |
| [**WindowsSubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Recupera uma substring da cadeia de caracteres especificada. A substring começa na posição de caractere especificada. |
| [**WindowsSubstringWithSpecifiedLength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Recupera uma substring da cadeia de caracteres especificada. A subcadeia de caracteres começa em uma posição de caractere especificado e tem um comprimento especificado. |
| [**WindowsTrimStringEnd**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Remove todas as ocorrências à frente de um conjunto especificado de caracteres da cadeia de caracteres de origem. |
| [**WindowsTrimStringStart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Remove todas as ocorrências à frente de um conjunto especificado de caracteres da cadeia de caracteres de origem. |



 

 

 

---
title: arquivos de biblioteca e Configurações de compilador
description: arquivos de biblioteca e Configurações de compilador
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows SDK do formato de mídia, arquivos de biblioteca
- Windows SDK do formato de mídia, configurações do compilador
- Windows SDK do formato de mídia, arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176f6c7acb9516e8c7ac38a067091bcbb0c8f7cf49cfdb9e65b396768158b233
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930656"
---
# <a name="library-files-and-compiler-settings"></a>arquivos de biblioteca e Configurações de compilador

para desenvolver um aplicativo usando o SDK do formato de mídia Windows, você deve usar Microsoft Visual C++ versão 6,0 ou posterior. As únicas linguagens de programação apropriadas para o desenvolvimento são C++ e C.

O conteúdo dos vários arquivos de cabeçalho incluídos neste SDK é descrito na tabela a seguir.



| Arquivo de cabeçalho                 | Descrição                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asreferenciar. h                    | Define códigos de erro relacionados a operações de arquivo ASF. Esse cabeçalho está incluído em WMSDK. h.                                                                                                                                                            |
| drmexternals. h              | Define estruturas, enumerações e constantes usadas para DRM (gerenciamento de direitos digitais). Inclua esse cabeçalho ao escrever um aplicativo que usa DRM.                                                                                            |
| dshowasf. h                  | define os filtros do Microsoft DirectShow QASF. inclua esse cabeçalho ao gravar um aplicativo DirectShow que cria ou lê arquivos ASF. para obter mais informações, consulte [DirectShow e Windows mídia](directshow-and-windows-media.md).               |
| msnetobj. h                  | define a interface [**IRMGetLicense**](irmgetlicense.md) , que é implementada em uma das bibliotecas de tempo de execução instaladas com o SDK do formato de mídia Windows.                                                                                     |
| NSError. h                   | define códigos de erro para Windows tecnologias de mídia. somente um subconjunto desses códigos de erro são relevantes para o SDK do formato de mídia Windows. Esse cabeçalho está incluído em WMSDK. h.                                                                            |
| wmdxva. h                    | inclui outros cabeçalhos e definições necessários para habilitar a aceleração de vídeo do Microsoft DirectX para reprodução de conteúdo baseado em mídia Windows. Para obter mais informações, consulte [habilitando a aceleração de vídeo do DirectX](enabling-directx-video-acceleration.md). |
| wmnetsourcecreator. h        | Contém as informações necessárias para criar plug-ins de origem de rede.                                                                                                                                                                                      |
| wmsbuffer. h                 | Define as interfaces usadas por objetos de buffer. Inclua esse cabeçalho ao criar seus próprios buffers para leitura de arquivos.                                                                                                                                 |
| WMSDK. h                     | o cabeçalho principal para aplicativos que usam o SDK do formato de mídia Windows. Este cabeçalho não contém definições, mas inclui asreferenciation. h, NSError. h, Windows. h e wmsdkidl. h. Incluir este cabeçalho para todos os aplicativos que usam este SDK.                     |
| wmsdkidl. h                  | define as interfaces, as funções, as estruturas, as enumerações e as constantes para a maioria dos objetos do SDK do formato de mídia Windows. Esse cabeçalho está incluído em WMSDK. h.                                                                             |
| wmsinternaladminnetsource. h | Define as interfaces dos plug-ins de origem da rede.                                                                                                                                                                                                  |
| wmsysprf. h                  | Define as constantes para os perfis de sistema. Inclua esse cabeçalho em aplicativos que carregam perfis de sistema por identificador.                                                                                                                         |



 

para usar o SDK do formato de mídia Windows, seu compilador deve ser configurado corretamente. A configuração é diferente para a criação no modo de depuração do que para o modo de versão. Defina sua configuração de acordo com a tabela a seguir. todas essas configurações são definidas na caixa de diálogo Project Configurações. para acessar a caixa de diálogo, selecione **Configurações** no menu **Project** .



| Configuração                                                                 | Valor de depuração                                                                              | Valor da versão                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Guia C/C++, categoria = geração de código) Usar biblioteca de tempo de execução            | Depurar DLL multithread                                                                  | DLL multithread                                                                       |
| (Guia link, categoria = geral) Ignorar todas as bibliotecas padrão (caixa de seleção) | Selecionada                                                                                 | Selecionada                                                                                |
| (Guia link, categoria = geral) Módulos de objeto/biblioteca                   | Inclua MSVCRTD. lib e Wmvcore.lib.Do não incluem libc. lib ou qualquer variação.<br/> | Inclua msvcrt. lib e Wmvcore.lib.Do não incluem libc. lib ou qualquer variação.<br/> |



 

se você estiver usando Microsoft Visual Studio .net, as configurações foram alteradas para locais diferentes, conforme mostrado na tabela a seguir. Todas essas configurações são definidas na caixa de diálogo **páginas de propriedades** . Para acessar a caixa de diálogo, clique com o botão direito do mouse no seu projeto no painel de **Gerenciador de soluções** e selecione **Propriedades** no menu de contexto.



| Configuração                                                                  | Valor de depuração                                                                              | Valor da versão                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Propriedades de configuração/C/C++/geração de código) Biblioteca de tempo de execução     | DLL de depuração multi-threaded (/MDd)                                                          | DLL multi-threaded (/MD)                                                                |
| (Propriedades de configuração/vinculador/entrada) Dependências adicionais      | Inclua MSVCRTD. lib e Wmvcore.lib.Do não incluem libc. lib ou qualquer variação.<br/> | Inclua msvcrt. lib e Wmvcore.lib.Do não incluem libc. lib ou qualquer variação.<br/> |
| (Propriedades de configuração/vinculador/entrada) Ignorar todas as bibliotecas padrão | Sim                                                                                      | Sim                                                                                     |



 

se você quiser atrasar o carregamento de Wmvcore.dll, ou qualquer outra DLL, use a opção de link/DELAYLOAD no Microsoft Visual C++ 6,0 ou atrase DLLs carregadas no Microsoft Visual C++ .net.

além disso, você precisa incluir os diretórios para as bibliotecas e cabeçalhos do SDK do formato de mídia Windows. Para localizar as configurações de diretório para Visual C++ 6,0, no menu **ferramentas** , clique em **Opções** e, em seguida, clique na guia **diretórios** . ao usar o Visual C++ .net, clique em **opções** no menu **ferramentas** e selecione projetos/VC++ diretórios na lista de opções. Adicione diretórios conforme mostrado na tabela a seguir. se você alterou o diretório de instalação para o SDK do formato de mídia Windows, seu caminho será diferente.



| Tipo de diretório | Caminho padrão                 |
|----------------|------------------------------|
| Incluir arquivos  | C: \\ WMSDK \\ WMFSDK11 \\ include |
| Arquivos de biblioteca  | C: \\ WMSDK \\ WMFSDK11 \\ lib     |



 

Se você estiver usando o SDK da plataforma, os caminhos padrão aparecerão da seguinte maneira:



| Tipo de diretório | Caminho padrão                                              |
|----------------|-----------------------------------------------------------|
| Incluir arquivos  | C: \\ arquivos de programas \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ incluem |
| Arquivos de biblioteca  | C: \\ arquivos de programas \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ Lib     |



 

Antes de chamar qualquer uma das funções de criação, COM deve ser inicializado com uma chamada para **CoInitialize** ou **CoinitializeEx**. O modelo de Threading livre ou o modelo Apartment Threading pode ser usado, mas o modelo de Threading Apartment impõe restrições de threading no aplicativo. Para obter mais informações sobre o Microsoft Component Object Model (COM), consulte a página COM no [site da Microsoft](../com/the-component-object-model.md).

**Observação** Aplicativos que reproduzem ou criam arquivos protegidos por DRM (Rights Management digital) exigem uma biblioteca estática individualizada que deve ser obtida separadamente da Microsoft. para obter mais informações, consulte o formulário licenciamento de mídia Windows no [site da Microsoft](https://www.microsoft.com/licensing/default). Se você usar a biblioteca DRM, não deverá vincular a WMVCORE. lib.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](getting-started.md)
</dt> </dl>

 


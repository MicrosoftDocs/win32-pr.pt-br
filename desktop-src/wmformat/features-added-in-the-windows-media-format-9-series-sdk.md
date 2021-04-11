---
title: Recursos adicionados no SDK da série Windows Media Format 9 Series
description: Recursos adicionados no SDK da série Windows Media Format 9 Series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- SDK do Windows Media Format, recursos
- SDK do Windows Media Format, novos recursos
- SDK do Windows Media Format, leitores síncronos
- SDK do Windows Media Format, indexação baseada em quadros
- SDK do Windows Media Format, códigos de tempo SMPTE
- SDK do Windows Media Format, filtros do DirectShow
- SDK do Windows Media Format, recurso de gravação de DRM
- SDK do Windows Media Format, coletores de arquivos
- SDK do Windows Media Format, DXVA (aceleração de vídeo do DirectX)
- SDK do Windows Media Format, áudio multicanal
- SDK do Windows Media Format, marca d' água
- SDK do Windows Media Format, suporte a vários idiomas
- SDK do Windows Media Format, modelos de conformidade do dispositivo
- SDK do Windows Media Format, enumerações de codec
- SDK do Windows Media Format, exclusão mútua
- SDK do Windows Media Format, taxa de bits múltipla (MBR)
- SDK do Windows Media Format, transcodificação com recompactação inteligente
- SDK do Windows Media Format, recompactação inteligente
- SDK do Windows Media Format, recompactação
- SDK do Windows Media Format, metadados
- SDK do Windows Media Format, taxa de proporção de pixels dinâmicos
- SDK do Windows Media Format, fluxos de vídeo entrelaçados
- Windows Media Format SDK, codificação em duas passagens
- SDK do Windows Media Format, WMStub. lib
- leitores síncronos, sobre
- indexação baseada em quadros
- Códigos de tempo SMPTE, sobre
- Filtros do DirectShow
- coletores de arquivos, aprimoramentos
- áudio de multicanal, sobre
- marca d' água, sobre
- codecs, enumerações
- exclusão mútua, sobre
- DRM (gerenciamento de direitos digitais), capacidade de gravação
- DRM (gerenciamento de direitos digitais), capacidade de gravação
- DXVA (aceleração de vídeo do DirectX), sobre
- DXVA (aceleração de vídeo DirectX), sobre
- ASF (Advanced Systems Format), suporte a vários idiomas
- ASF (formato de sistemas avançados), suporte a vários idiomas
- taxa de bits múltipla (MBR), sobre
- MBR (taxa de bits múltipla), sobre
- transcodificação com recompactação inteligente
- recompactação inteligente
- recompactação
- metadados, Windows Media Format SDK
- taxa de proporção de pixels dinâmicos
- fluxos de vídeo entrelaçados
- codificação de dois passos, sobre
- 2-passar codificação, sobre
- WMStub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159874"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a><span data-ttu-id="60344-153">Recursos adicionados no SDK da série Windows Media Format 9 Series</span><span class="sxs-lookup"><span data-stu-id="60344-153">Features Added in the Windows Media Format 9 Series SDK</span></span>

<span data-ttu-id="60344-154">O SDK do Windows Media Format 9 Series introduziu muitos aprimoramentos e recursos.</span><span class="sxs-lookup"><span data-stu-id="60344-154">The Windows Media Format 9 Series SDK introduced many improvements and features.</span></span> <span data-ttu-id="60344-155">Esta seção fornece uma visão geral desses recursos para o benefício dos usuários de migrar de uma versão anterior do SDK.</span><span class="sxs-lookup"><span data-stu-id="60344-155">This section provides an overview of those features for the benefit of users migrating from an earlier version of the SDK.</span></span>

## <a name="synchronous-reading"></a><span data-ttu-id="60344-156">Leitura síncrona</span><span class="sxs-lookup"><span data-stu-id="60344-156">Synchronous Reading</span></span>

<span data-ttu-id="60344-157">Você pode ler arquivos ASF com chamadas síncronas.</span><span class="sxs-lookup"><span data-stu-id="60344-157">You can read ASF files with synchronous calls.</span></span> <span data-ttu-id="60344-158">Ao ler um arquivo de forma síncrona, você pode alterar as configurações do leitor enquanto ele está sendo lido.</span><span class="sxs-lookup"><span data-stu-id="60344-158">When reading a file synchronously, you can change the settings of the reader while it is reading.</span></span> <span data-ttu-id="60344-159">As operações de leitura síncronas do SDK não oferecem suporte para a leitura de arquivos pela Internet, mas você pode usar a interface COM padrão, **IStream**, para ler de fontes personalizadas.</span><span class="sxs-lookup"><span data-stu-id="60344-159">The synchronous reading operations of the SDK do not provide support for reading files over the Internet, but you can use the standard COM interface, **IStream**, to read from custom sources.</span></span>

## <a name="frame-based-indexing"></a><span data-ttu-id="60344-160">Indexação baseada em quadros</span><span class="sxs-lookup"><span data-stu-id="60344-160">Frame-based Indexing</span></span>

<span data-ttu-id="60344-161">Você pode indexar arquivos ASF com base em quadros de vídeo.</span><span class="sxs-lookup"><span data-stu-id="60344-161">You can index ASF files based on video frames.</span></span> <span data-ttu-id="60344-162">O leitor e o leitor síncrono podem buscar um quadro de um fluxo de vídeo e sincronizar os outros fluxos para esse quadro.</span><span class="sxs-lookup"><span data-stu-id="60344-162">Both the reader and the synchronous reader can seek to a frame of a video stream and synchronize the other streams to that frame.</span></span>

## <a name="indexing-and-seeking-with-smpte-time-code"></a><span data-ttu-id="60344-163">Indexação e busca com o código de tempo SMPTE</span><span class="sxs-lookup"><span data-stu-id="60344-163">Indexing and Seeking with SMPTE Time Code</span></span>

<span data-ttu-id="60344-164">O SDK do Windows Media Format permite armazenar códigos de tempo SMPTE em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="60344-164">The Windows Media Format SDK enables you to store SMPTE time codes in ASF files.</span></span> <span data-ttu-id="60344-165">Os arquivos podem ser indexados pelo código de hora SMPTE, e o leitor assíncrono e o leitor síncrono podem buscar entradas de índice de código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="60344-165">Files can be indexed by SMPTE time code, and both the asynchronous reader and synchronous reader can seek to SMPTE time code index entries.</span></span>

## <a name="directshow-filters"></a><span data-ttu-id="60344-166">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="60344-166">DirectShow Filters</span></span>

<span data-ttu-id="60344-167">O SDK do Windows Media Format inclui dois filtros de® do Microsoft DirectShow que permitem que aplicativos baseados em DirectShow leiam e gravem arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="60344-167">The Windows Media Format SDK includes two Microsoft DirectShow® filters that enable DirectShow-based applications to read and write ASF files.</span></span> <span data-ttu-id="60344-168">O DirectShow também permite que os aplicativos capturem dados de dispositivos de vídeo de áudio e descompactem dados de uma variedade de formatos antes de codificá-los novamente como conteúdo baseado no Windows Media.</span><span class="sxs-lookup"><span data-stu-id="60344-168">DirectShow also enables applications to capture data from audio-video devices and decompress data from a variety of formats before re-encoding it as Windows Media-based content.</span></span>

## <a name="enhanced-profiles"></a><span data-ttu-id="60344-169">Perfis avançados</span><span class="sxs-lookup"><span data-stu-id="60344-169">Enhanced Profiles</span></span>

<span data-ttu-id="60344-170">Os perfis podem conter informações de compartilhamento de largura de banda e informações de priorização de fluxo.</span><span class="sxs-lookup"><span data-stu-id="60344-170">Profiles can contain bandwidth sharing information and stream prioritization information.</span></span> <span data-ttu-id="60344-171">O compartilhamento de largura de banda permite especificar que dois ou mais fluxos, independentemente de suas taxas de bits individuais, nunca usarão mais do que uma quantidade especificada de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="60344-171">Bandwidth sharing enables you to specify that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth.</span></span> <span data-ttu-id="60344-172">A largura de banda que compartilha os dados em um perfil é puramente informativa; Ele não é imposto por nenhuma lógica no SDK.</span><span class="sxs-lookup"><span data-stu-id="60344-172">The bandwidth sharing data in a profile is purely informational; it is not enforced by any logic in the SDK.</span></span> <span data-ttu-id="60344-173">A priorização de fluxo permite que você especifique uma ordem de prioridade para os fluxos em um perfil.</span><span class="sxs-lookup"><span data-stu-id="60344-173">Stream prioritization enables you to specify an order of priority for the streams in a profile.</span></span> <span data-ttu-id="60344-174">Se não houver largura de banda suficiente na reprodução para transmitir o arquivo corretamente, os fluxos de prioridade mais baixos poderão ser ignorados para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="60344-174">If there is not enough bandwidth at playback to stream the file properly, the lowest priority streams can be ignored in order to improve performance.</span></span>

## <a name="drm-writing-capability"></a><span data-ttu-id="60344-175">Funcionalidade de gravação de DRM</span><span class="sxs-lookup"><span data-stu-id="60344-175">DRM Writing Capability</span></span>

<span data-ttu-id="60344-176">Além do suporte a leitura de DRM existente, o SDK do Windows Media Format 9 Series adicionou suporte para gravar arquivos ASF com a proteção DRM versão 1 ou DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="60344-176">In addition to the existing DRM-reading support, the Windows Media Format 9 Series SDK added support for writing ASF files with either DRM version 1 or DRM version 7 protection.</span></span> <span data-ttu-id="60344-177">Essa nova funcionalidade habilita cenários de "DRM ao vivo", como webcast de pagamento por exibição de eventos esportivos vivos ou concertos.</span><span class="sxs-lookup"><span data-stu-id="60344-177">This new capability enables "Live DRM" scenarios such as pay-per-view webcasting of live sporting events or concerts.</span></span>

## <a name="enhanced-file-sink"></a><span data-ttu-id="60344-178">Coletor de arquivo avançado</span><span class="sxs-lookup"><span data-stu-id="60344-178">Enhanced File Sink</span></span>

<span data-ttu-id="60344-179">Vários novos recursos de coletor de arquivos foram adicionados à versão 9 Series do SDK.</span><span class="sxs-lookup"><span data-stu-id="60344-179">Several new file sink capabilities were added to the 9 Series version of the SDK.</span></span> <span data-ttu-id="60344-180">Você pode configurar o coletor de arquivos para desabilitar a indexação automática de arquivos ASF criados recentemente.</span><span class="sxs-lookup"><span data-stu-id="60344-180">You can configure the file sink to disable automatic indexing of newly created ASF files.</span></span> <span data-ttu-id="60344-181">Você também tem a opção de configurá-lo para entrada e saída sem buffer.</span><span class="sxs-lookup"><span data-stu-id="60344-181">You also have the option to configure it for unbuffered input and output.</span></span>

## <a name="directx-video-acceleration"></a><span data-ttu-id="60344-182">Aceleração de vídeo do DirectX</span><span class="sxs-lookup"><span data-stu-id="60344-182">DirectX Video Acceleration</span></span>

<span data-ttu-id="60344-183">A DXVA (aceleração de vídeo do DirectX) é uma tecnologia que permite a reprodução de vídeo de alta taxa de bits (qualidade de DVD ou melhor) em computadores menos poderosos com placas gráficas habilitadas para DXVA.</span><span class="sxs-lookup"><span data-stu-id="60344-183">DirectX Video Acceleration (DXVA) is a technology that enables playback of high-bit-rate video (DVD quality or better) on less powerful machines with DXVA-enabled graphics cards.</span></span> <span data-ttu-id="60344-184">Você pode usar o objeto leitor deste SDK para habilitar a aceleração de vídeo do DirectX, se o hardware oferecer suporte a ele, ao reproduzir arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="60344-184">You can use the reader object of this SDK to enable DirectX Video Acceleration, if the hardware supports it, when playing ASF files.</span></span>

## <a name="multichannel-audio"></a><span data-ttu-id="60344-185">Áudio de multicanal</span><span class="sxs-lookup"><span data-stu-id="60344-185">Multichannel Audio</span></span>

<span data-ttu-id="60344-186">Você pode codificar e reproduzir áudio multicanal.</span><span class="sxs-lookup"><span data-stu-id="60344-186">You can encode and play multichannel audio.</span></span> <span data-ttu-id="60344-187">O codec Windows Media Audio 9 Professional dá suporte a formatos com 6 canais e 8 canais, bem como estéreo de alta definição.</span><span class="sxs-lookup"><span data-stu-id="60344-187">The Windows Media Audio 9 Professional codec supports formats with 6 channels and 8 channels as well as high definition stereo.</span></span>

## <a name="watermarking"></a><span data-ttu-id="60344-188">Marca d' água</span><span class="sxs-lookup"><span data-stu-id="60344-188">Watermarking</span></span>

<span data-ttu-id="60344-189">Você pode codificar arquivos ASF com marcas d' água digitais para segurança.</span><span class="sxs-lookup"><span data-stu-id="60344-189">You can encode ASF files with digital watermarks for security.</span></span> <span data-ttu-id="60344-190">Todos os sistemas de marca d' água são diferentes em sua abordagem, mas toda a identificação de inserção no conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="60344-190">All watermarking systems are different in their approach, but all embed identification into encoded content.</span></span> <span data-ttu-id="60344-191">A marca d' água é executada usando DMOs (objetos de mídia) do® DirectX de terceiros especiais.</span><span class="sxs-lookup"><span data-stu-id="60344-191">Watermarking is performed using special third-party DirectX® media objects (DMOs).</span></span>

## <a name="support-for-multiple-languages-in-asf-files"></a><span data-ttu-id="60344-192">Suporte para vários idiomas em arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="60344-192">Support for Multiple Languages in ASF files</span></span>

<span data-ttu-id="60344-193">Você pode dar suporte a vários idiomas em arquivos ASF, em fluxos e em metadados.</span><span class="sxs-lookup"><span data-stu-id="60344-193">You can support multiple languages in ASF files, both in streams and in metadata.</span></span> <span data-ttu-id="60344-194">Por exemplo, você pode criar um arquivo de vídeo com fluxos de áudio em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="60344-194">For example, you can create a video file with audio streams in several languages.</span></span> <span data-ttu-id="60344-195">Na reprodução, o usuário pode selecionar qual idioma usar ou o aplicativo pode consultar as informações do sistema no computador de jogo e selecionar um idioma automaticamente.</span><span class="sxs-lookup"><span data-stu-id="60344-195">At playback, the user can select which language to use, or your application can query the system information on the playing computer and select a language automatically.</span></span> <span data-ttu-id="60344-196">Os atributos de metadados também podem ser inseridos várias vezes, com os valores em idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="60344-196">Metadata attributes can also be entered multiple times, with the values in different languages.</span></span>

## <a name="device-conformance-templates"></a><span data-ttu-id="60344-197">Modelos de conformidade do dispositivo</span><span class="sxs-lookup"><span data-stu-id="60344-197">Device Conformance Templates</span></span>

<span data-ttu-id="60344-198">Para auxiliar no direcionamento de conteúdo para dispositivos cliente específicos, os codecs de mídia do Windows agora dão suporte a modelos de conformidade de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60344-198">To assist in targeting content to specific client devices, the Windows Media codecs now support device conformance templates.</span></span> <span data-ttu-id="60344-199">Cada modelo contém um intervalo definido de configurações e recursos de codec que devem ser usados para a mídia destinada a uma determinada categoria de plataformas.</span><span class="sxs-lookup"><span data-stu-id="60344-199">Each template contains a defined range of settings and codec features that should be used for media intended for a particular category of platforms.</span></span> <span data-ttu-id="60344-200">Não há mais suporte para perfis de sistema com as versões mais recentes dos codecs de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="60344-200">System profiles are no longer supported with the latest versions of the Windows Media codecs.</span></span> <span data-ttu-id="60344-201">Todos os perfis devem ser personalizados para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="60344-201">All profiles must be customized to suit your needs.</span></span> <span data-ttu-id="60344-202">Você pode usar modelos de conformidade do dispositivo para ajudá-lo a criar seus perfis.</span><span class="sxs-lookup"><span data-stu-id="60344-202">You can use device conformance templates to assist you in designing your profiles.</span></span>

## <a name="expanded-codec-enumeration"></a><span data-ttu-id="60344-203">Enumeração de codec expandida</span><span class="sxs-lookup"><span data-stu-id="60344-203">Expanded Codec Enumeration</span></span>

<span data-ttu-id="60344-204">O objeto Gerenciador de perfis pode consultar os codecs de vídeo e áudio do Windows Media para obter os formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="60344-204">The profile manager object can query the Windows Media Audio and Video codecs for supported formats.</span></span> <span data-ttu-id="60344-205">Você pode definir parâmetros para os formatos recuperados.</span><span class="sxs-lookup"><span data-stu-id="60344-205">You can set parameters for the formats retrieved.</span></span> <span data-ttu-id="60344-206">Por exemplo, você pode recuperar todos os formatos de taxa de bits variáveis com base em qualidade suportados pelo codec do Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="60344-206">For example, you can retrieve all the quality-based variable bit rate formats supported by the Windows Media Audio 9 codec.</span></span>

## <a name="improved-mutual-exclusion"></a><span data-ttu-id="60344-207">Exclusão mútua aprimorada</span><span class="sxs-lookup"><span data-stu-id="60344-207">Improved Mutual Exclusion</span></span>

<span data-ttu-id="60344-208">Você pode criar registros nomeados contendo vários fluxos dentro de um objeto de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="60344-208">You can create named records containing multiple streams within a mutual exclusion object.</span></span> <span data-ttu-id="60344-209">Você também pode nomear objetos de exclusão mútua para torná-los mais fáceis de identificar.</span><span class="sxs-lookup"><span data-stu-id="60344-209">You can also name mutual exclusion objects to make them easier to identify.</span></span> <span data-ttu-id="60344-210">Isso permite que você crie camadas de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="60344-210">This enables you to create layers of mutual exclusion.</span></span> <span data-ttu-id="60344-211">Por exemplo, um arquivo pode conter fluxos mutuamente exclusivos por taxa de bits e por idioma.</span><span class="sxs-lookup"><span data-stu-id="60344-211">For example, a file can contain streams that are mutually exclusive by bit rate and by language.</span></span> <span data-ttu-id="60344-212">A exclusão mútua baseada em linguagem envolveria grupos de fluxos, cada grupo consistindo em fluxos no mesmo idioma, mas mutuamente exclusivos por taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="60344-212">The language-based mutual exclusion would involve groups of streams, each group consisting of streams in the same language but mutually exclusive by bit rate.</span></span>

## <a name="expanded-multiple-bit-rate-support"></a><span data-ttu-id="60344-213">Suporte à taxa de vários bits expandido</span><span class="sxs-lookup"><span data-stu-id="60344-213">Expanded Multiple Bit Rate Support</span></span>

<span data-ttu-id="60344-214">O suporte à exclusão mútua está incluído para áudio de taxa de bits múltipla (MBR) e para vídeo com fluxos de tamanhos de imagem variados.</span><span class="sxs-lookup"><span data-stu-id="60344-214">Mutual exclusion support is included for multiple bit rate (MBR) audio and for video with streams of varying image sizes.</span></span>

## <a name="attributes-for-streams"></a><span data-ttu-id="60344-215">Atributos para fluxos</span><span class="sxs-lookup"><span data-stu-id="60344-215">Attributes for Streams</span></span>

<span data-ttu-id="60344-216">Você pode atribuir atributos a fluxos individuais em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="60344-216">You can assign attributes to individual streams in ASF files.</span></span> <span data-ttu-id="60344-217">Você ainda deve usar atributos de nível de arquivo para arquivos MP3.</span><span class="sxs-lookup"><span data-stu-id="60344-217">You must still use file-level attributes for MP3 files.</span></span> <span data-ttu-id="60344-218">Esse recurso não adiciona nenhum método ao SDK, mas os métodos existentes agora aceitam números de fluxo diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="60344-218">This feature does not add any methods to the SDK, but the existing methods will now accept stream numbers other than zero.</span></span>

## <a name="transcoding-with-smart-recompression"></a><span data-ttu-id="60344-219">Transcodificação com recompactação inteligente</span><span class="sxs-lookup"><span data-stu-id="60344-219">Transcoding with Smart Recompression</span></span>

<span data-ttu-id="60344-220">A recompactação inteligente permite que você transcodifique arquivos de áudio do Windows Media de uma taxa de bits alta para uma taxa de bits inferior com melhor qualidade do que o que era alcançado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="60344-220">Smart recompression allows you to transcode Windows Media audio files from a high bit rate to a lower bit rate with better quality than previously achievable.</span></span>

## <a name="expanded-metadata-support"></a><span data-ttu-id="60344-221">Suporte a metadados expandido</span><span class="sxs-lookup"><span data-stu-id="60344-221">Expanded Metadata Support</span></span>

<span data-ttu-id="60344-222">O Windows Media Format SDK fornece os seguintes novos recursos de metadados:</span><span class="sxs-lookup"><span data-stu-id="60344-222">The Windows Media Format SDK provides the following new metadata features:</span></span>

-   <span data-ttu-id="60344-223">Marcas de metadados baseadas em índice, habilitando várias marcas com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="60344-223">Index-based metadata tags, enabling multiple tags with the same name.</span></span>
-   <span data-ttu-id="60344-224">Capacidade de ler atributos de cabeçalho DRM sem um arquivo WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="60344-224">Ability to read DRM header attributes without a WMStubDRM.lib file.</span></span>
-   <span data-ttu-id="60344-225">Atributos com mais de 64 quilobytes de dados associados.</span><span class="sxs-lookup"><span data-stu-id="60344-225">Attributes with more than 64 kilobytes of associated data.</span></span>
-   <span data-ttu-id="60344-226">Atributos em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="60344-226">Attributes in multiple languages.</span></span>
-   <span data-ttu-id="60344-227">Dezenas de novos atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="60344-227">Dozens of new predefined attributes.</span></span>

## <a name="dynamic-pixel-aspect-ratio"></a><span data-ttu-id="60344-228">Taxa de proporção de pixels dinâmicos</span><span class="sxs-lookup"><span data-stu-id="60344-228">Dynamic Pixel Aspect Ratio</span></span>

<span data-ttu-id="60344-229">Os fluxos de vídeo compostos por vários tipos de conteúdo podem ser acomodados identificando a taxa de proporção de pixel dos exemplos diferentes no fluxo.</span><span class="sxs-lookup"><span data-stu-id="60344-229">Video streams that are composed of various types of content can be accommodated by identifying the pixel aspect ratio of the disparate samples in the stream.</span></span> <span data-ttu-id="60344-230">Isso permite que o aplicativo de reprodução forneça uma reprodução melhor desse tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="60344-230">This enables the playing application to provide better playback of such content.</span></span>

## <a name="interlaced-video-streams"></a><span data-ttu-id="60344-231">Fluxos de vídeo entrelaçados</span><span class="sxs-lookup"><span data-stu-id="60344-231">Interlaced Video Streams</span></span>

<span data-ttu-id="60344-232">As versões anteriores do Windows Media Format SDK forneceram a capacidade de codificar o conteúdo [*entrelaçado*](wmformat-glossary.md) em um fluxo de vídeo de verificação progressiva.</span><span class="sxs-lookup"><span data-stu-id="60344-232">Previous versions of the Windows Media Format SDK have provided the ability to encode [*interlaced*](wmformat-glossary.md) content into a progressive-scan video stream.</span></span> <span data-ttu-id="60344-233">Começando com o SDK do Windows Media Format 9 Series, você pode codificar vídeo entrelaçado enquanto preserva seu formato entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="60344-233">Starting with the Windows Media Format 9 Series SDK, you can encode interlaced video while preserving its interlaced format.</span></span> <span data-ttu-id="60344-234">Isso pode resultar em uma reprodução aprimorada, especialmente em dispositivos entrelaçados, como conjuntos de televisão.</span><span class="sxs-lookup"><span data-stu-id="60344-234">This can result in improved playback, particularly on interlaced devices, such as television sets.</span></span>

## <a name="two-pass-encoding"></a><span data-ttu-id="60344-235">Codificação de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="60344-235">Two-Pass Encoding</span></span>

<span data-ttu-id="60344-236">Os novos codecs de mídia do Windows habilitam a codificação de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="60344-236">The new Windows Media codecs enable two-pass encoding.</span></span> <span data-ttu-id="60344-237">O conteúdo codificado em duas passagens pode atingir uma saída de qualidade mais alta.</span><span class="sxs-lookup"><span data-stu-id="60344-237">Content encoded in two passes can achieve higher quality output.</span></span>

## <a name="new-speech-codec"></a><span data-ttu-id="60344-238">Novo codec de fala</span><span class="sxs-lookup"><span data-stu-id="60344-238">New Speech Codec</span></span>

<span data-ttu-id="60344-239">Esse SDK inclui o novo codec de voz do Windows Media Audio 9 que é otimizado para codificar a voz humana enquanto usa uma taxa de bits baixa.</span><span class="sxs-lookup"><span data-stu-id="60344-239">This SDK includes the new Windows Media Audio 9 Voice codec which is optimized for encoding the human voice while using a low bit rate.</span></span> <span data-ttu-id="60344-240">Esse codec também fornece um desempenho superior para conteúdo misto de voz musical.</span><span class="sxs-lookup"><span data-stu-id="60344-240">This codec also provides superior performance for mixed music-voice content.</span></span>

## <a name="accessible-video-frame-duration"></a><span data-ttu-id="60344-241">Duração do quadro de vídeo acessível</span><span class="sxs-lookup"><span data-stu-id="60344-241">Accessible Video Frame Duration</span></span>

<span data-ttu-id="60344-242">Você pode ter o objeto gravador desse SDK para fornecer a duração dos quadros de vídeo ao leitor.</span><span class="sxs-lookup"><span data-stu-id="60344-242">You can have the writer object of this SDK provide the duration of video frames to the reader.</span></span>

## <a name="streaming-html"></a><span data-ttu-id="60344-243">HTML de streaming</span><span class="sxs-lookup"><span data-stu-id="60344-243">Streaming HTML</span></span>

<span data-ttu-id="60344-244">Com a versão anterior deste SDK, você pôde usar um comando de script para sinalizar seu aplicativo para abrir uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="60344-244">With previous version of this SDK, you were able to use a script command to signal your application to open a Web page.</span></span> <span data-ttu-id="60344-245">Começando com o SDK do Windows Media Format 9 Series, você pode armazenar os componentes de páginas da Web em seus arquivos ASF, para garantir que não haja nenhum atraso nas apresentações.</span><span class="sxs-lookup"><span data-stu-id="60344-245">Starting with the Windows Media Format 9 Series SDK, you can store the components of Web pages in your ASF files, to ensure that there is no lag in presentations.</span></span>

## <a name="wmstublib-no-longer-required-for-build-environment"></a><span data-ttu-id="60344-246">WMStub. lib não é mais necessário para o ambiente de compilação</span><span class="sxs-lookup"><span data-stu-id="60344-246">WMStub.lib no longer required for build environment</span></span>

<span data-ttu-id="60344-247">As configurações de ambiente de compilação para o SDK do Windows Media Format foram alteradas a partir do SDK do Windows Media Format 9 Series.</span><span class="sxs-lookup"><span data-stu-id="60344-247">The build-environment settings for the Windows Media Format SDK changed starting with the Windows Media Format 9 Series SDK.</span></span> <span data-ttu-id="60344-248">Você não precisa mais incluir WMStub. lib para aplicativos que usam esse SDK.</span><span class="sxs-lookup"><span data-stu-id="60344-248">You no longer need to include WMStub.lib for applications using this SDK.</span></span> <span data-ttu-id="60344-249">No entanto, os aplicativos habilitados para DRM ainda devem obter e assinar um contrato de licença separado e obter uma biblioteca estática exclusiva da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60344-249">However, DRM-enabled applications still must obtain and sign a separate license agreement, and obtain a unique static library from Microsoft.</span></span> <span data-ttu-id="60344-250">Entre em contato wmla@microsoft.com para obter mais informações sobre a biblioteca DRM e o contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="60344-250">Contact wmla@microsoft.com for more information about the DRM library and license agreement.</span></span> <span data-ttu-id="60344-251">Para obter mais informações sobre como criar projetos com esse SDK, consulte [arquivos de biblioteca e configurações do compilador](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="60344-251">For more information about building projects with this SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="60344-252">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60344-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60344-253">**Sobre o SDK do Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="60344-253">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 





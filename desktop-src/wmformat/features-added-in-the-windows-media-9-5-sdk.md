---
title: Recursos adicionados no SDK do Windows Media 9,5
description: Recursos adicionados no SDK do Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- SDK do Windows Media Format, recursos
- SDK do Windows Media Format, novos recursos
- SDK do Windows Media Format, interface para processamento específico de aplicativo
- SDK do Windows Media Format, DXVA (aceleração de vídeo do DirectX)
- SDK do Windows Media Format, interface IWMPlayerHook
- IWMPlayerHook
- SDK do Windows Media Format, versões baseadas em x64 do Windows
- SDK do Windows Media Format, codec de imagem de vídeo do Windows Media
- SDK do Windows Media Format, codecs de áudio
- SDK do Windows Media Format, DRM 10 para dispositivos de rede
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, codec de perfil avançado
- SDK do Windows Media Format, formato de interconexão digital Sony/Philips (S/PDIF)
- SDK do Windows Media Format, formatos de atraso baixo
- SDK do Windows Media Format, modo de busca aproximado
- SDK do Windows Media Format, gravação da playlist
- SDK do Windows Media Format, suporte a vários idiomas
- SDK do Windows Media Format, SDK do Windows Media Gerenciador de Dispositivos
- SDK do Windows Media Format, interfaces de codec
- codecs, imagem de vídeo do Windows Media
- DRM (gerenciamento de direitos digitais), protocolo de transferência segura de dispositivos de rede
- DRM (gerenciamento de direitos digitais), protocolo de transferência segura de dispositivos de rede
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- codecs, codec de perfil avançado
- Formato de interconexão digital Sony/Philips (S/PDIF), transferindo ou transmitindo usando
- S/PDIF (formato de interconexão digital Sony/Philips), transferindo ou transmitindo usando
- modo de procura aproximado
- metadados, suporte a vários idiomas
- SDK do Windows Media Gerenciador de Dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084374"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a><span data-ttu-id="1ce8b-133">Recursos adicionados no SDK do Windows Media 9,5</span><span class="sxs-lookup"><span data-stu-id="1ce8b-133">Features Added in the Windows Media 9.5 SDK</span></span>

<span data-ttu-id="1ce8b-134">O SDK 9,5 do Windows Media Format apresentou novos recursos para fornecer segurança e flexibilidade de conteúdo aprimoradas.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-134">The Windows Media Format 9.5 SDK introduced new features to provide enhanced content security and flexibility.</span></span> <span data-ttu-id="1ce8b-135">As seguintes alterações foram feitas no SDK desde a versão da série 9.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-135">The following changes were made to the SDK since the 9 Series release.</span></span>

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a><span data-ttu-id="1ce8b-136">Nova interface para processamento específico do aplicativo durante aceleração de vídeo do DirectX</span><span class="sxs-lookup"><span data-stu-id="1ce8b-136">New Interface for Application-specific Processing During DirectX Video Acceleration</span></span>

<span data-ttu-id="1ce8b-137">Os aplicativos do Player que dão suporte à aceleração de vídeo do DirectX agora podem implementar a interface [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) para executar o processamento específico do aplicativo durante a decodificação do DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-137">Player applications that support DirectX Video Acceleration can now implement the [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) interface to perform application-specific processing during DirectX VA decoding.</span></span> <span data-ttu-id="1ce8b-138">O leitor chama o método de retorno de chamada [**IWMPLayerHook::P decodificar**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) antes de passar amostras de vídeo compactados para o processador de vídeo para decodificação.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-138">The reader calls the [**IWMPLayerHook::PreDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) callback method before passing compressed video samples to the video processor for decoding.</span></span>

> [!Note]  
> <span data-ttu-id="1ce8b-139">Para usar a interface **IWMPlayerHook** e a interface [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associada, você deve ter a atualização do número 888656 instalada no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-139">To use the **IWMPlayerHook** interface and the associated [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) interface, you must have update number 888656 installed in the Windows Media Format SDK.</span></span> <span data-ttu-id="1ce8b-140">Você pode baixar a atualização no [site da Microsoft](https://support.microsoft.com/?id=888656).</span><span class="sxs-lookup"><span data-stu-id="1ce8b-140">You can download the update from the [Microsoft Web site](https://support.microsoft.com/?id=888656).</span></span>

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a><span data-ttu-id="1ce8b-141">Versão do SDK do Windows Media Format para versões baseadas em x64 do Windows</span><span class="sxs-lookup"><span data-stu-id="1ce8b-141">Windows Media Format SDK version for x64-based versions of Windows</span></span>

<span data-ttu-id="1ce8b-142">Uma versão baseada em x64 do Windows Media Format SDK está disponível.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-142">An x64-based version of the Windows Media Format SDK is available.</span></span> <span data-ttu-id="1ce8b-143">Esta documentação se aplica às versões de 32 bits e à versão baseada em x64 do SDK.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-143">This documentation applies to both the 32-bit versions and the x64-based version of the SDK.</span></span> <span data-ttu-id="1ce8b-144">No entanto, o DRM (gerenciamento de direitos digitais) não tem suporte no SDK do Windows Media Format baseado em x64.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-144">However, digital rights management (DRM) is not supported in the x64-based Windows Media Format SDK.</span></span>

## <a name="new-version-of-the-windows-media-video-image-codec"></a><span data-ttu-id="1ce8b-145">Nova versão do codec de imagem de vídeo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="1ce8b-145">New Version of the Windows Media Video Image Codec</span></span>

<span data-ttu-id="1ce8b-146">O codec do Windows Media Video 9 Image v2 simplifica os cálculos de geometria de exemplo para panorâmica e zoom.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-146">The Windows Media Video 9 Image v2 codec simplifies the sample geometry calculations for panning and zooming.</span></span> <span data-ttu-id="1ce8b-147">O novo codec também dá suporte a várias transições complexas entre imagens.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-147">The new codec also supports several complex transitions between images.</span></span>

## <a name="new-version-of-the-windows-media-audio-codecs"></a><span data-ttu-id="1ce8b-148">Nova versão dos codecs de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="1ce8b-148">New Version of the Windows Media Audio Codecs</span></span>

<span data-ttu-id="1ce8b-149">O SDK 9,5 do Windows Media Format inclui os seguintes codecs de áudio atualizados:</span><span class="sxs-lookup"><span data-stu-id="1ce8b-149">The Windows Media Format 9.5 SDK includes the following updated audio codecs:</span></span>

-   <span data-ttu-id="1ce8b-150">Áudio do Windows Media 9,1</span><span class="sxs-lookup"><span data-stu-id="1ce8b-150">Windows Media Audio 9.1</span></span>
-   <span data-ttu-id="1ce8b-151">Windows Media Audio 9,1 Professional</span><span class="sxs-lookup"><span data-stu-id="1ce8b-151">Windows Media Audio 9.1 Professional</span></span>
-   <span data-ttu-id="1ce8b-152">Áudio do Windows Media 9,1 sem perdas</span><span class="sxs-lookup"><span data-stu-id="1ce8b-152">Windows Media Audio 9.1 Lossless</span></span>

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a><span data-ttu-id="1ce8b-153">Suporte ao protocolo Windows Media DRM 10 para dispositivos de rede</span><span class="sxs-lookup"><span data-stu-id="1ce8b-153">Windows Media DRM 10 for Network Devices Protocol Support</span></span>

<span data-ttu-id="1ce8b-154">O SDK 9,5 do Windows Media Format oferece suporte ao novo Windows Media DRM 10 para dispositivos de rede protocolo de transferência segura.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-154">The Windows Media Format 9.5 SDK supports the new Windows Media DRM 10 for Network Devices secure transfer protocol.</span></span> <span data-ttu-id="1ce8b-155">Esse protocolo pode ser usado para transmitir conteúdo criptografado por uma rede local para um dispositivo de reprodução, como um receptor de vídeo de conjunto superior.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-155">This protocol can be used to stream encrypted content over a local network to a playback device, such as a set-top video receiver.</span></span>

<span data-ttu-id="1ce8b-156">A maioria dos procedimentos usados para implementar o suporte para Windows Media DRM 10 para dispositivos de rede deve ser executada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-156">Most of the procedures used to implement support for Windows Media DRM 10 for Network Devices must be performed by the application.</span></span> <span data-ttu-id="1ce8b-157">No entanto, você pode usar métodos do Windows Media Format SDK para fornecer a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="1ce8b-157">However, you can use methods of the Windows Media Format SDK to provide the following functionality:</span></span>

-   <span data-ttu-id="1ce8b-158">Mantenha um banco de dados de dispositivos, incluindo aqueles habilitados para o Windows Media DRM 10 para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-158">Maintain a database of devices, including those that are enabled for Windows Media DRM 10 for Network Devices.</span></span>
-   <span data-ttu-id="1ce8b-159">Valide dispositivos para garantir que eles sejam "perto" o suficiente para o cliente na rede para transmissão segura.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-159">Validate devices to ensure that they are "near" enough to the client on the network for secure streaming.</span></span>
-   <span data-ttu-id="1ce8b-160">Converta arquivos protegidos por DRM no Windows Media DRM 10 para fluxos de dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-160">Convert DRM-protected files to Windows Media DRM 10 for Network Devices streams.</span></span>
-   <span data-ttu-id="1ce8b-161">Gravar arquivos usando dados anteriormente criptografados.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-161">Write files using previously encrypted data.</span></span>

## <a name="support-for-new-drm-licenses"></a><span data-ttu-id="1ce8b-162">Suporte para novas licenças DRM</span><span class="sxs-lookup"><span data-stu-id="1ce8b-162">Support for New DRM Licenses</span></span>

<span data-ttu-id="1ce8b-163">As novas licenças criadas usando o SDK do Windows Media Rights Manager usam níveis de proteção de saída (OPLs) para especificar direitos e restrições para reproduzir e copiar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-163">New licenses created by using the Windows Media Rights Manager SDK use Output Protection Levels (OPLs) to specify rights and restrictions for playing and copying content.</span></span> <span data-ttu-id="1ce8b-164">O Windows Media Format SDK fornece suporte para a leitura do OPLs de uma licença.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-164">The Windows Media Format SDK provides support for reading the OPLs from a license.</span></span>

## <a name="new-video-codec"></a><span data-ttu-id="1ce8b-165">Novo codec de vídeo</span><span class="sxs-lookup"><span data-stu-id="1ce8b-165">New Video Codec</span></span>

<span data-ttu-id="1ce8b-166">O codec de perfil avançado do Windows Media Video 9 baseia-se na alta qualidade do codec do Windows Media Video 9 ao adicionar suporte para codificação entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-166">The Windows Media Video 9 Advanced Profile codec builds on the high quality of the Windows Media Video 9 codec while adding support for interlaced encoding.</span></span>

## <a name="spdif-output"></a><span data-ttu-id="1ce8b-167">Saída de S/PDIF</span><span class="sxs-lookup"><span data-stu-id="1ce8b-167">S/PDIF Output</span></span>

<span data-ttu-id="1ce8b-168">O conteúdo codificado com um dos codecs do Windows Media Audio Professional agora pode ser transferido ou transmitido usando o S/PDIF (formato de interconexão digital) da Sony/Philips.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-168">Content encoded with one of the Windows Media Audio Professional codecs can now be transferred or transmitted using the Sony/Philips Digital Interconnect Format (S/PDIF).</span></span>

## <a name="low-delay-audio"></a><span data-ttu-id="1ce8b-169">Low-Delay áudio</span><span class="sxs-lookup"><span data-stu-id="1ce8b-169">Low-Delay Audio</span></span>

<span data-ttu-id="1ce8b-170">Os codecs do Windows Media Audio 9,1 e Windows Media Audio 9,1 Professional agora oferecem suporte a vários formatos de atraso baixo.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-170">The Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs now each support several low-delay formats.</span></span> <span data-ttu-id="1ce8b-171">Esses formatos produzem fluxos de áudio que podem ser iniciados mais rapidamente, reduzindo a latência em cenários de alternância de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-171">These formats produce audio streams that can be started more quickly, reducing latency in stream-switching scenarios.</span></span> <span data-ttu-id="1ce8b-172">A latência geral em transmissões ao vivo também é melhorada com o uso de formatos de atraso baixo.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-172">Overall latency in live broadcasts is also improved by using low-delay formats.</span></span>

## <a name="approximate-seeking-mode"></a><span data-ttu-id="1ce8b-173">Modo de procura aproximado</span><span class="sxs-lookup"><span data-stu-id="1ce8b-173">Approximate Seeking Mode</span></span>

<span data-ttu-id="1ce8b-174">Agora você pode buscar um tempo aproximado em um arquivo ASF com o leitor.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-174">You can now seek to an approximate time in an ASF file with the reader.</span></span> <span data-ttu-id="1ce8b-175">Esse modo melhora o desempenho ao executar uma busca imprecisa, como quando um usuário clica na barra de busca no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-175">This mode improves performance when performing an imprecise seek, such as when a user clicks the seek bar in Windows Media Player.</span></span> <span data-ttu-id="1ce8b-176">A busca aproximada retorna o exemplo de mídia para o cleanpoint anterior em vez de reconstruir o exemplo para o tempo preciso procurado.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-176">Approximate seeking returns the media sample for the previous cleanpoint instead of reconstructing the sample for the precise time sought.</span></span>

## <a name="playlist-burning"></a><span data-ttu-id="1ce8b-177">Gravação de playlist</span><span class="sxs-lookup"><span data-stu-id="1ce8b-177">Playlist Burning</span></span>

<span data-ttu-id="1ce8b-178">O Windows Media DRM 10 dá suporte a direitos de cópia de arquivos de áudio para um CD de livro vermelho como parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-178">Windows Media DRM 10 supports rights for copying audio files to Red Book CD as part of a playlist.</span></span> <span data-ttu-id="1ce8b-179">O Windows Media Format SDK fornece métodos para verificar se os arquivos em uma playlist têm permissão para serem copiados.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-179">The Windows Media Format SDK provides methods for verifying whether the files in a playlist are allowed to be copied.</span></span>

## <a name="improved-multiple-language-support-for-metadata"></a><span data-ttu-id="1ce8b-180">Suporte de Multiple-Language aprimorado para metadados</span><span class="sxs-lookup"><span data-stu-id="1ce8b-180">Improved Multiple-Language Support for Metadata</span></span>

<span data-ttu-id="1ce8b-181">No SDK do Windows Media Format 9 Series, todos os metadados adicionados a um arquivo foram atribuídos a uma lista de idiomas que recebeu o identificador de idioma do idioma padrão.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-181">In the Windows Media Format 9 Series SDK, all metadata added to a file was assigned to a language list that was given the language identifier of the default language.</span></span> <span data-ttu-id="1ce8b-182">Isso causou problemas quando os distribuidores de conteúdo em localidades diferentes adicionavam alguns metadados, porque os usuários na localidade do distribuidor só veem os poucos atributos adicionados para seu idioma.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-182">This caused problems when content distributors in different locales added some metadata, because users in the distributor's locale only see the few attributes added for their language.</span></span> <span data-ttu-id="1ce8b-183">O SDK 9,5 do Windows Media Format resolve esse problema não criando uma lista de idiomas até que haja atributos de dois idiomas presentes no arquivo.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-183">The Windows Media Format 9.5 SDK solves this problem by not creating a language list until there are attributes from two languages present in the file.</span></span> <span data-ttu-id="1ce8b-184">Nesse ponto, todos os metadados são associados à localidade do segundo idioma, que, em seguida, torna-se o padrão.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-184">At that point, all of the metadata is associated with the locale of the second language, which then becomes the default.</span></span> <span data-ttu-id="1ce8b-185">Dessa forma, um distribuidor de conteúdo pode manter todos os metadados originais de um arquivo, como título e autor, intactos ao adicionar alguns atributos pertinentes à sua localidade.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-185">In this way, a content distributor can keep all of the original metadata for a file, such as title and author, intact while adding some attributes pertinent to their locale.</span></span>

## <a name="windows-media-device-manager-sdk-included-in-installation"></a><span data-ttu-id="1ce8b-186">SDK do Windows Media Gerenciador de Dispositivos incluído na instalação</span><span class="sxs-lookup"><span data-stu-id="1ce8b-186">Windows Media Device Manager SDK Included in Installation</span></span>

<span data-ttu-id="1ce8b-187">O pacote de instalação do Windows Media Format 9,5 SDK instala o SDK do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-187">The installation package for the Windows Media Format 9.5 SDK installs the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="1ce8b-188">A documentação do SDK do Windows Media Gerenciador de Dispositivos pode ser encontrada na pasta C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (sua pasta será diferente se você não instalar o SDK do formato de mídia do Windows na pasta padrão.)</span><span class="sxs-lookup"><span data-stu-id="1ce8b-188">The documentation for the Windows Media Device Manager SDK can be found in the C:\\WMSDK\\WMFSDK95\\WMDM\\docs folder (your folder will be different if you do not install the Windows Media Format SDK in the default folder.)</span></span>

## <a name="codec-interface-documentation"></a><span data-ttu-id="1ce8b-189">Documentação da interface do codec</span><span class="sxs-lookup"><span data-stu-id="1ce8b-189">Codec Interface Documentation</span></span>

<span data-ttu-id="1ce8b-190">Esta documentação inclui informações sobre como usar os codecs de áudio e vídeo do Windows Media fora do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-190">This documentation includes information about using the Windows Media Audio and Video codecs outside of the Windows Media Format SDK.</span></span> <span data-ttu-id="1ce8b-191">Esta documentação foi lançada originalmente como parte de um download da Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-191">This documentation was originally released as part of a download from the Microsoft Developer Network.</span></span> <span data-ttu-id="1ce8b-192">Os aplicativos de exemplo que demonstram o uso do codec DMOs diretamente estão incluídos na instalação do SDK do Windows Media Format juntamente com os cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="1ce8b-192">The sample applications that demonstrate using the codec DMOs directly are included in the Windows Media Format SDK installation along with headers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ce8b-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ce8b-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ce8b-194">**Sobre o SDK do Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="1ce8b-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 





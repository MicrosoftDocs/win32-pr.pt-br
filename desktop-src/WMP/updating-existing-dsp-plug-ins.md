---
title: Atualizando plug-ins de DSP existentes
description: Atualizando plug-ins de DSP existentes
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- plug-ins Windows Media Player, processamento de sinal digital (DSP)
- plug-ins, processamento de sinal digital (DSP)
- plug-ins de processamento de sinal digital, atualizando
- Plug-ins do DSP, atualizando
- versões do Windows Media Player, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725a7a752206f4d321af9deb106df82c40b677dd719182660c5940cac4788244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122726"
---
# <a name="updating-existing-dsp-plug-ins"></a>Atualizando plug-ins de DSP existentes

plug-ins do DSP criados antes do lançamento do SDK do Windows Media Player 11 podem não funcionar conforme o esperado com o Windows Media Player 11 em execução no Windows Vista. para garantir que os clientes que executam o Windows Media Player 11 no Windows Vista possam usar seus plug-ins, você deve fazer algumas alterações no código de plug-in do DSP, recompilar seu projeto e distribuir o plug-in atualizado para seus clientes.

os projetos criados com a versão mais recente do assistente de plug-in de Windows Media Player conterá as atualizações necessárias. consulte [atualizações para o assistente de Plug-in do DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md). (é uma boa ideia executar o assistente para criar um novo projeto de exemplo e, em seguida, usar uma ferramenta como Windiff.exe, que vem com Visual Studio, para inspecionar as diferenças entre o código de exemplo e o código de produção).

Há três alterações principais que você precisará fazer em qualquer plug-in de DSP existente:

-   Altere a maneira como o plug-in registra. Seu plug-in existente provavelmente registrará o modelo de Threading como "Apartment". o Windows Media Player 11 em execução no Windows Vista requer que os plug-ins do DSP registrem o modelo de threading como "ambos". Você pode corrigir isso alterando o valor do modelo de threading no arquivo *ProjectName*. rgs, da seguinte maneira:

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > Especificar o modelo de Threading como "both" remove qualquer serialização que o COM forneça para chamadas para interfaces personalizadas. Se você fizer chamadas para suas interfaces personalizadas de vários threads, deverá fornecer essa serialização por conta própria.

     

    o Windows Media Player 11 garante que as chamadas para interfaces de DMO sejam serializadas corretamente.

    1.  Adicionar chamadas a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) com um novo tipo de plug-in: WMP \_ plugintype \_ DSP \_ OUTOFPROC em DllRegisterServer e DllUnregisterServer no seu arquivo *projectnamedll*. cpp. Consulte as páginas de referência para esses métodos para obter detalhes.
    2.  Crie e distribua uma DLL de proxy/stub para habilitar o marshaling COM de qualquer interface personalizada implementada ou criada pela classe de plug-in. Uma interface personalizada é qualquer interface proprietária que você define e implementa para uso pelo objeto de plug-in. Isso inclui a interface personalizada usada por sua página de propriedades, se você tiver fornecido uma, mas também pode incluir interfaces que se conectam a plug-ins de interface do usuário, por exemplo. Um exemplo de interface personalizada criada pelo assistente de plug-in é *Iprojectname*. Exemplos de interfaces que não são interfaces personalizadas incluem **IMediaObject** e **IWMPPluginEnable**.

Se o plug-in do DSP processar áudio, você também deverá adicionar suporte para os seguintes novos formatos de áudio:

-   \_formato Wave \_ IEEE \_ float
-   \_Formato Wave \_ extensível com SUBformato KSDATAFORMAT \_ subtipo \_ IEEE \_ float.

Se o plug-in do DSP processar vídeo, você deverá adicionar suporte para o formato de vídeo NV12.

Consulte o plug-in de exemplo de áudio ou vídeo DSP que o assistente cria para obter um exemplo de como processar esses tipos de formato.

## <a name="about-the-proxystub-project"></a>Sobre o Project de proxy/stub

Talvez a maneira mais simples de criar um projeto de DLL de proxy/stub para seu plug-in do DSP seja executar o assistente de plug-in do DSP. Isso criará um exemplo de projeto de proxy/stub que você pode modificar para trabalhar com seu código existente. Você precisará fazer as seguintes alterações:

1.  Remova todas as definições existentes para suas interfaces personalizadas do seu código. por exemplo, o assistente de plug-in do DSP do SDK do Windows Media Player 10 criou a definição da interface *Iprojectname* no arquivo *projectname*. h usando a palavra-chave **interface** .
2.  Defina suas interfaces personalizadas no arquivo IDL do projeto de proxy/stub.
3.  Crie o projeto de proxy/stub antes do projeto principal. você pode configurar Visual Studio para fazer isso automaticamente se ambos os projetos fizerem parte da mesma solução.
4.  O compilador MIDL criará um novo arquivo de cabeçalho com um nome no formato *ProjectName* \_ h.h. Você deve incluir esse cabeçalho em seu projeto principal (no *ProjectName*. h). Ele contém as definições para suas interfaces personalizadas.

## <a name="distributing-the-updated-plug-in"></a>Distribuindo o plug-in atualizado

Você pode instalar o plug-in atualizado nos computadores dos usuários exatamente como no passado. No entanto, agora você também deve distribuir e registrar a DLL de proxy/stub.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 





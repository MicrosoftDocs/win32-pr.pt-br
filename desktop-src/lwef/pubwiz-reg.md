---
title: Registrando um serviço
description: Para adicionar seu serviço à lista de provedores no Assistente de Publicação na Web ou no Assistente de Ordenação de Impressão Online, você deve adicionar a chave apropriada e seus valores ao Windows Registro.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- register,services
- Assistente de Publicação na Web, registrando
- Assistente de Ordenação de Impressão Online, registrando
- register,Assistente de Publicação na Web
- register,Assistente de Ordenação de Impressão Online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f5e3f43fe981558fcbf8573eb8768646f112f4816486159cc7c16d71e40e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608636"
---
# <a name="registering-a-service"></a>Registrando um serviço

Para adicionar seu serviço à lista de provedores no Assistente de Publicação na Web ou no Assistente de Ordenação de Impressão Online, você deve adicionar a chave apropriada e seus valores ao Windows Registro.

## <a name="required-keys-and-values"></a>Chaves e valores necessários

Para adicionar seu serviço à lista de provedores para o Assistente de Publicação na Web, adicione uma chave, conforme mostrado abaixo.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Para adicionar seu serviço à lista de provedores para o Assistente de Ordenação de Impressão Online, adicione uma chave, conforme mostrado abaixo.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Cada um dos valores é uma cadeia de caracteres do tipo REG \_ SZ. Forneça seus dados conforme explicado na tabela a seguir. 

| Nome do valor     | Explicação                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | O caminho completo para o arquivo de ícone, incluindo o nome do arquivo.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | O nome exibido para o serviço na lista de provedores do assistente.                                                                                                                                                                                                                                                                                                                                                             |
| Descrição    | Uma breve descrição para seu serviço. Essa descrição também é exibida na lista de provedores do assistente diretamente abaixo do nome do serviço.                                                                                                                                                                                                                                                                                    |
| Href           | A URL da primeira página do serviço.                                                                                                                                                                                                                                                                                                                                                                                      |
| Supportedtypes | Os tipos de arquivo com suporte pelo serviço. Por exemplo, *\*.jpg*. Especificando apenas determinados tipos de arquivo, seu serviço só aparece quando esses tipos de arquivo foram selecionados. Se mais de um tipo de arquivo tiver sido selecionado, seu serviço será exibido se qualquer um desses tipos de arquivo tiver suporte do serviço. Se você quiser especificar vários tipos de arquivo, separe-os na lista com ponto e vírgula. Por exemplo, *\*.jpg; \*.bmp*. |



 

A seguir está um exemplo completo para um serviço de processamento de fotos intitulado "MyProvider".

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

Quando a URL do serviço é chamada, dois valores são adicionados ao final da URL – lcid e langid. Por exemplo, a cadeia de caracteres de URL para o exemplo acima pode ser https: \/ /www.MyProvider.com/Intro.htm?lcid=1033&langid=1033. Essas variáveis são usadas para informações de idioma e localização.

-   **lcid** é usado para informar o servidor das configurações de país/região e idioma do cliente. Ele não é usado para determinar o idioma da interface do usuário do cliente, mas é usado para determinar o formato adequado para moeda, data e hora e outros dados específicos da região.
-   **langid** é usado para informar o servidor da configuração de idioma padrão do cliente para que ele possa usar o idioma adequado na interface do usuário.

 

 





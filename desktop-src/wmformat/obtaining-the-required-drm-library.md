---
title: Obtendo a biblioteca de DRM necessária
description: Obtendo a biblioteca de DRM necessária
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- SDK do Windows Media Format, obtendo as bibliotecas de DRM necessárias
- ASF (Advanced Systems Format), obtendo as bibliotecas de DRM necessárias
- ASF (formato de sistemas avançados), obtendo as bibliotecas de DRM necessárias
- DRM (gerenciamento de direitos digitais), obtendo bibliotecas necessárias
- DRM (gerenciamento de direitos digitais), obtendo bibliotecas necessárias
- DRM (gerenciamento de direitos digitais), informações de compilação
- DRM (gerenciamento de direitos digitais), informações de compilação
- DRM (gerenciamento de direitos digitais), informações de depuração
- DRM (gerenciamento de direitos digitais), informações de depuração
- Depurando DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c124c1e7edf0bba736b9dd392e852aac97e96
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366847"
---
# <a name="obtaining-the-required-drm-library"></a>Obtendo a biblioteca de DRM necessária

Para criar ou reproduzir arquivos de mídia digital protegidos por DRM, seu aplicativo deve vincular a uma biblioteca estática que é fornecida em formato binário pela Microsoft. Essa biblioteca, às vezes, é chamada de biblioteca de stubs ou "stublib" e identifica exclusivamente seu aplicativo.

Nesta documentação, a biblioteca DRM é conhecida como "WMStubDRM. lib". O nome da biblioteca que você receberá incluirá um número de identificação. Para obter essa biblioteca, você deve assinar um contrato de licença com a Microsoft. Os termos do contrato podem diferir dependendo se você solicitar uma licença de avaliação ou uma licença de produção. Para obter mais informações sobre o processo de licenciamento DRM, consulte o formulário licenciamento do Windows Media no [site da Microsoft](https://www.microsoft.com/licensing/default).

A biblioteca que você recebe tem um nível de segurança de DRM que depende do tipo de contrato de licença inserido. Uma licença DRM pode restringir aplicativos com componentes DRM abaixo de um nível de segurança especificado de acessar o conteúdo do arquivo. Esse nível de segurança não é o mesmo que o nível de individualização DRM, nem está relacionado a nenhum dos valores numéricos dos níveis de proteção de saída (OPLs). A tabela a seguir mostra exemplos de níveis de segurança do DRM para diferentes jogadores e dispositivos portáteis.



| Nível de segurança | Players e dispositivos portáteis                                                                                                                                                                                                                                                                                                   | Exemplo                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 150            | Dispositivos que não dão suporte ao Windows Media DRM. A proteção de DRM é removida quando o conteúdo é transferido para um dispositivo desse tipo.                                                                                                                                                                                                         | Dispositivos que dão suporte ao conteúdo baseado no Windows Media, mas não conteúdo protegido                                                                                                                       |
| 1,000          | Aplicativos de Player baseados no Windows Media Format 9,5 SDK ou anterior que não atendem aos requisitos adicionais para o nível 2000. dispositivos baseados em DRM v1 do dispositivo portátil do Windows Media.<br/> Dispositivos com base no Windows CE 4,2 e posterior.<br/>                                                                       | Windows Media Player 6,4, dispositivos de mídia 7Portable do Windows Media Player que dão suporte ao Windows Media portátil do dispositivo DRM v1.<br/>                                                             |
| 2\.000          | Aplicativos de Player baseados no SDK da série Windows Media Format 9 Series ou posterior e que seguem um conjunto mais estrito de diretrizes de proteção de conteúdo do que aplicativos em nível 1000. dispositivos baseados no Windows Media DRM 10 para dispositivos portáteis.<br/> Dispositivos baseados no Windows Media DRM 10 para dispositivos de rede.<br/> | Dispositivos de mídia do Windows Media Player 9 Series e laterPortable que dão suporte ao Windows Media DRM 10 para dispositivos portáteis<br/> Dispositivos portáteis do Media Center baseados no Windows Mobile<br/> |



 

## <a name="build-and-debugging-information"></a>Informações de compilação e depuração

Quando você vincula a WMStubDRM. lib, não vincule a WMVCORE. lib. O componente DRM não funcionará corretamente se o aplicativo for vinculado a ambas as bibliotecas.

Um ponto de interrupção do usuário no componente DRM impedirá que as versões de depuração e de lançamento dos aplicativos acessem o conteúdo protegido durante a execução dentro do depurador. Para solucionar problemas de funções relacionadas ao DRM em seu aplicativo, você deve escrever suas próprias rotinas de rastreamento que salvam informações como valores **HRESULT** em algum local, como um arquivo de log.

Se você tentar executar uma versão de lançamento de um aplicativo em um sistema com uma versão de depuração dos bits do SDK instalado (ou o contrário), encontrará erros de heap durante a reprodução do conteúdo do DRM versão 7. Certifique-se de executar depurar aplicativos por bits do SDK de depuração e liberar aplicativos em bits de lançamento. O mesmo problema ocorrerá se você executar uma versão de depuração do SDK com um componente DRM individual (que é sempre uma compilação de versão).

**Observações** do O DRM não é compatível com a versão baseada em x64 deste SDK.

Os arquivos WMStubDRM. lib associados ao SDK 9,5 do Windows Media Format podem ser usados somente com os componentes do Microsoft Visual Studio .NET 2003. Se você estiver usando uma versão mais antiga da biblioteca de stub, não haverá nenhuma nova restrição para seu uso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 






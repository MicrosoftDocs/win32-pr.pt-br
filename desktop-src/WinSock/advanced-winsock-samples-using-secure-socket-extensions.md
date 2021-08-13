---
description: Exemplos de Winsock avançados usando extensões de soquete seguro
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Exemplos de Winsock avançados usando extensões de soquete seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ead38a7e62be527e91474ac921803327647ca6cefd1ec68778d03e1c68c1bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412166"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Exemplos de Winsock avançados usando extensões de soquete seguro

## <a name="secure-tcp-client-and-server-sample"></a>Exemplo de cliente e servidor de TCP seguro

um exemplo de Winsock mais avançado que demonstra o uso de extensões de soquete seguro está incluído no SDK (Software Development Kit) do Microsoft Windows. O exemplo inclui um cliente TCP e um servidor que se conectam com segurança usando o Winsock e as extensões de soquete seguro.

Por padrão, o código-fonte de exemplo do Winsock é instalado no seguinte diretório:

*C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ amostras \\ NetDs \\ winsock*

Um exemplo está localizado na seguinte pasta:

*securesocket*

O código de exemplo é dividido em diretórios separados, conforme descrito abaixo:

-   stcpclient-a pasta que contém o código de cliente TCP seguro.
-   stcpcommon-a pasta que contém o código de biblioteca comum que é compartilhado entre o cliente e o servidor de TCP seguro.
-   stcpserver-a pasta que contém o código do servidor TCP seguro.

deve-se observar que os exemplos devem ser executados em dois computadores diferentes que executam o Windows Vista ou posterior. Além disso, as credenciais IPsec devem ser provisionadas em ambos os computadores para que a conexão seja realizada com sucesso, pois o exemplo usa IPsec para proteger seu tráfego. Consulte a documentação sobre configuração de [IPSec](/windows/desktop/FWP/ipsec-configuration) para obter mais informações sobre como configurar credenciais IPSec.

A criação do exemplo irá gerar dois arquivos executáveis:

*stcpclient.exe* e *stcpserver.exe*.

Copie *stcpclient.exe* para o computador a e copie *stcpserver.exe* para o computador B. No computador B, inicie o servidor TCP executando o seguinte em um prompt de comando:

**stcpserver.exe**

Execute o seguinte comando para obter mais opções de uso para o servidor:

**stcpserver.exe/?**

Em seguida, no computador A, inicie o cliente TCP executando o seguinte em um prompt de comando:

**stcpclient.exe <totalmente qualificado-DNS-name-for-Machine-B>**

Neste ponto, a conexão deve ser estabelecida com segurança.

Execute o seguinte comando para obter mais opções de uso para o cliente:

**stcpclient.exe/?**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[sobre a plataforma de filtragem de Windows](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Aplicação da camada de aplicativo (EPA)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[Configuração de IPsec](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[Funções IPsec](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Usando extensões de soquete seguro](using-secure-socket-extensions.md)
</dt> <dt>

[SSPI (interface do provedor de suporte de segurança)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Plataforma de filtragem do Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Windows Funções da API de plataforma de filtragem](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Extensões do Winsock Secure Socket](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 

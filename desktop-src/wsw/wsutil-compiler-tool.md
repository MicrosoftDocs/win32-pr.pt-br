---
title: Ferramenta de compilador do WsUtil
description: A ferramenta do compilador do Windows Web Services, WsUtil.exe, dá suporte ao modelo de serviço e à serialização de tipos de dados. Ele processa documentos WSDL, de esquema XML e de política e gera cabeçalhos C e arquivos de origem.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Serviços Web da ferramenta de compilador WsUtil para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917798"
---
# <a name="wsutil-compiler-tool"></a>Ferramenta de compilador do WsUtil

A ferramenta do compilador do Windows Web Services, WsUtil.exe, dá suporte ao [modelo de serviço](service-model-layer-overview.md) e à [serialização](serialization.md) de tipos de dados. Ele processa documentos WSDL, de esquema XML e de política e gera cabeçalhos C e arquivos de origem. Essa ferramenta é semelhante à ferramenta de compilador WSDL para código gerenciado, mas é destinada a código nativo em vez disso.

Para dar suporte ao [modelo de serviço](service-model-layer-overview.md), WsUtil.exe gera cabeçalhos a serem usados tanto para o cliente quanto para o serviço. Ele gera o arquivo de proxy C para o lado do cliente e os arquivos stub C para o lado do serviço, conforme necessário.

Para dar suporte à [serialização](serialization.md), o compilador gera cabeçalhos para as descrições de elemento para definições de elementos globais e todas as informações de definição de tipo nos arquivos de proxy consumidos pelo mecanismo de serialização.


Para obter opções de linha de comando para processar arquivos WSDL, arquivos de esquema XML e arquivos de política de serviço Web, consulte os seguintes tópicos:

-   [Ferramenta de compilador de serviço Web](web-service-compiler-tool.md)
-   [Contratos de serviço e WSDL](wsdl-support.md)
-   [Suporte de esquema](schema-support.md)
-   [Suporte de política](policy-support.md)

## <a name="security"></a>Segurança

Ao usar o WsUtil, esteja atento aos seguintes problemas e observe as precauções apropriadas:

-   Wsutil não recupera metadados XML pela rede e Wsutil não resolve as instruções import e/ou include nos arquivos de metadados de entrada. Wsutil abre e lê arquivos WSDL, XSD e de política. Os metadados XML não são resistentes a adulterações. Certifique-se de usar somente arquivos WSDL, XSD e de política são adquiridos da fonte confiável e certifique-se de proteger os arquivos contra violação antes e depois de usá-los. Examine atentamente o conteúdo dos arquivos de entrada e valide se o conteúdo dos arquivos é seguro para uso no aplicativo. Wsutil.exe não realiza nenhuma verificação de autenticidade dos arquivos de metadados.
-   O Wsutil gera arquivos de cabeçalho e stub, que não são resistentes a adulterações. Você precisa definir os direitos de acesso de nível correto em arquivos de origem gerados pelo wsutil.exe para impedir o acesso unauthoritized a esses arquivos. Wsutil usa System. IO. StreamWriter para criar os arquivos de saída.
-   Os usuários precisam estar cientes de que o Wsutil pode substituir seus arquivos locais e deve ter cuidado para especificar nomes de arquivos e diretórios seguros para arquivos de saída usando a opção/out.
-   Wsutil ou wsutilhelper.dll carregado na wsutil.exe, pode ser encerrado inesperadamente ou consumir uma grande quantidade de recursos do sistema quando estiver sob ataque ou no processamento de uma quantidade muito grande de metadados de entrada. A ferramenta foi projetada para ser usada durante o tempo de desenvolvimento apenas essa ferramenta deve ser usada apenas como uma ferramenta de tempo de desenvolvimento. Ele pode não ser seguro para uso na camada intermediária para processar informações de política.
-   Wsutilhelper.dll DLL auxiliar é carregado em wsutil.exe gerenciado para processar informações de política. O usuário deve garantir que nenhum binário mal-intencionado com o mesmo nome de arquivo exista no caminho binário. Da mesma forma, o usuário deve ter certeza no ambiente de compilação, o caminho binário está configurado corretamente, pois não há nenhum binário mal-intencionado com o mesmo nome "wsutil.exe".
-   O Wsutil gera a anotação SAL para os campos de operações e estrutura quando possível. O usuário de arquivos gerados pelo Wsutil deve seguir o requisito especificado por meio da anotação SAL.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da camada do modelo de serviço](service-model-layer-overview.md)
</dt> <dt>

[Série](serialization.md)
</dt> <dt>

[Ferramenta de compilador de serviço Web](web-service-compiler-tool.md)
</dt> <dt>

[Suporte a WSDL](wsdl-support.md)
</dt> <dt>

[Suporte de esquema](schema-support.md)
</dt> <dt>

[Suporte de política](policy-support.md)
</dt> </dl>

 

 





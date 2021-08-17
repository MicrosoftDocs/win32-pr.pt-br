---
title: Ferramenta compilador WsUtil
description: A Windows do compilador de Serviços Web, WsUtil.exe, dá suporte ao modelo de serviço e à serialização de tipos de dados. Ele processa documentos WSDL, esquema XML e política e gera os arquivos de origem e os títulos C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Serviços Web da ferramenta compilador WsUtil para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9a4e5761a068e991463451595c410c01f868d4d3e6c9df6ab25a7cb232d678
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119324896"
---
# <a name="wsutil-compiler-tool"></a>Ferramenta compilador WsUtil

A Windows do compilador de Serviços Web, WsUtil.exe, dá suporte ao modelo de serviço [e](service-model-layer-overview.md) [à serialização](serialization.md) de tipos de dados. Ele processa documentos WSDL, esquema XML e política e gera os arquivos de origem e os títulos C. Essa ferramenta é semelhante à ferramenta do compilador WSDL para código gerenciado, mas destina-se ao código nativo.

Para dar suporte [ao modelo de](service-model-layer-overview.md)serviço , WsUtil.exe gera os headers a serem usados para o cliente e o serviço. Ele gera o arquivo proxy C para o lado do cliente e arquivos stub C para o lado do serviço, conforme necessário.

Para dar suporte à [serialização](serialization.md), o compilador gera os headers para descrições de elemento para definições de elemento global e todas as informações de definição de tipo nos arquivos proxy consumidos pelo mecanismo de serialização.


Para opções de linha de comando para processar arquivos WSDL, arquivos de esquema XML e arquivos de política de serviço Web, consulte os seguintes tópicos:

-   [Ferramenta compilador de serviço Web](web-service-compiler-tool.md)
-   [WSDL e contratos de serviço](wsdl-support.md)
-   [Suporte de esquema](schema-support.md)
-   [Suporte à política](policy-support.md)

## <a name="security"></a>Segurança

Ao usar o WsUtil, esteja ciente dos seguintes problemas e observe as precauções apropriadas:

-   O Wsutil não recupera metadados XML pela rede e wsutil não resolve instruções de importação e/ou inclusão nos arquivos de metadados de entrada. O Wsutil abre e lê os arquivos wsdl, xsd e policy. Os metadados XML não são resistentes a adulterações. Certifique-se de que você use apenas os arquivos wsdl, xsd e policy adquiridos da fonte confiável e proteja os arquivos contra adulterações antes e depois de usá-los. Revise cuidadosamente o conteúdo dos arquivos de entrada e valide se o conteúdo dos arquivos é seguro para uso no aplicativo. Wsutil.exe não faz nenhuma verificação de autenticidade dos arquivos de metadados.
-   O Wsutil gera arquivos de stub e de título, que não são resistentes a adulterações. Você precisa definir os direitos de acesso de nível correto em arquivos de origem gerados pelo wsutil.exe para impedir o acesso não autorizado a esses arquivos. O Wsutil usa System.IO.StreamWriter para criar os arquivos de saída.
-   Os usuários precisam estar cientes de que o Wsutil pode substituir seus arquivos locais e devem ter cuidado para especificar nomes de arquivo e diretórios seguros para arquivos de saída usando a opção /out.
-   O Wsutil ou wsutilhelper.dll carregado no wsutil.exe, pode terminar inesperadamente ou consumir uma grande quantidade de recursos do sistema quando sob ataque ou no processamento de uma grande quantidade de metadados de entrada. A ferramenta foi projetada para ser usada somente durante o tempo de desenvolvimento. Essa ferramenta deve ser usada apenas como uma ferramenta de tempo de desenvolvimento. Pode não ser seguro para uso na camada intermediária processar informações de política.
-   Wsutilhelper.dll DLL auxiliar é carregada no wsutil.exe para processar informações de política. O usuário deve garantir que não exista nenhum binário mal-intencionado com o mesmo nome de arquivo no caminho binário. Da mesma forma, o usuário deve garantir que, no ambiente de build, o caminho binário seja configurado corretamente de que não há binário mal-intencionado com o mesmo nome "wsutil.exe".
-   O Wsutil gera a anotação SAL para operações e campos de estrutura quando possível. O usuário dos arquivos gerados pelo wsutil deve seguir o requisito especificado por meio da anotação SAL.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da camada do modelo de serviço](service-model-layer-overview.md)
</dt> <dt>

[Serialização](serialization.md)
</dt> <dt>

[Ferramenta compilador de serviço Web](web-service-compiler-tool.md)
</dt> <dt>

[Suporte a WSDL](wsdl-support.md)
</dt> <dt>

[Suporte de esquema](schema-support.md)
</dt> <dt>

[Suporte à política](policy-support.md)
</dt> </dl>

 

 





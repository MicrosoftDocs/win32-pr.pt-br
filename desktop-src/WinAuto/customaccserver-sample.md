---
title: Exemplo de CustomAccServer
description: Exemplo de CustomAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088004"
---
# <a name="customaccserver-sample"></a>Exemplo de CustomAccServer

Este tópico inclui as seções a seguir.

-   [Descrição](#description)
-   [Informações de download](#download-information)
-   [Requisitos mínimos](#minimum-requirements)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo mostra como implementar um Microsoft Acessibilidade Ativa Server para um controle personalizado simples. O objeto acessível para o controle consiste no elemento raiz (uma caixa de listagem) e seus filhos (os itens de lista).

## <a name="download-information"></a>Informações de download

O exemplo CustomAccServer é instalado como parte do [SDK (Software Development Kit) do Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) e está disponível no local a seguir.



| Local    | Caminho/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| SDK do Windows | % Arquivos de programas% \\ Microsoft SDKs \\ Windows número de \\ \[ versão \] \\ amostras \\ WinUI \\ MSAA |



 

## <a name="minimum-requirements"></a>Requisitos mínimos



| Produto          | Versão                         |
|------------------|---------------------------------|
| Sistema operacional | Windows XP, Windows Server 2003 |
| SDK do Windows      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo usando o Visual Studio 2008:

1.  Execute a ferramenta de configuração do SDK (Software Development Kit) do Microsoft Windows fornecida com o SDK para adicionar diretórios de inclusão do SDK ao Visual Studio.
2.  Abra o Windows Explorer e navegue até o diretório do projeto.
3.  Clique duas vezes no ícone do arquivo. sln (solução) para abrir o projeto no Visual Studio.
4.  No menu **Compilar** , selecione **Compilar solução** para compilar a solução. O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.

Para criar o exemplo na linha de comando, consulte Criando exemplos no SDK do Windows notas de versão no seguinte local:% Arquivos de programas% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo:

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  Digite AccServer.exe na linha de comando ou clique duas vezes no ícone de AccServer.exe para iniciá-lo no Windows Explorer.

Para executar a partir do Visual Studio, pressione F5 ou clique em **Iniciar Depuração** no menu **depurar** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras](samples.md)
</dt> </dl>

 

 





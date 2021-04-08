---
title: Sistema de arquivos projetado pelo Windows
description: Visão geral do sistema de arquivos projetado do Windows (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 8391ec63f23c9ebae5b47e4cac862f6ab3079ceb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823808"
---
# <a name="windows-projected-file-system-projfs"></a>Sistema de arquivos projetado do Windows (ProjFS)

O sistema de arquivos projetado do Windows (ProjFS) permite que um aplicativo de modo de usuário chamado "provedor" faça o projeto de dados hierárquicos de um armazenamento de dados de backup no sistema de arquivos, fazendo com que ele apareça como arquivos e diretórios no sistema de arquivos. Por exemplo, um provedor simples pode projetar o registro do Windows no sistema de arquivos, fazendo com que as chaves e os valores do registro apareçam como arquivos e diretórios, respectivamente. Um exemplo de um provedor mais complexo é o [VFS para git](https://github.com/Microsoft/VFSForGit), que é usado para virtualizar repositórios git muito grande.

> [!NOTE]
> O ProjFS foi projetado para uso com armazenamentos de dados de backup de alta velocidade. Uma de suas metas de design é fazer com que os dados projetados apareçam como se estivessem presentes localmente, ocultando o fato de que os dados podem ser remotos. Como tal, o ProjFS não fornece: mecanismos para relatar o progresso da recuperação de dados; indicação do estado online versus offline de um arquivo; nem outros recursos que podem ser desejáveis ao trabalhar com armazenamentos de dados de backup lentos. Para esses cenários, considere usar a [API de arquivos de nuvem](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                                                       | Descrição |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Guia de programação do sistema de arquivos projetado pelo Windows](projfs-programming-guide.md)                              | Informações conceituais sobre como implementar um aplicativo de provedor ProjFS.
| [Referência da API do sistema de arquivos projetadas do Windows](projfs-reference.md)                                          | Informações de referência para a interface de programação ProjFS.
| [Glossário do sistema de arquivos projetado do Windows](projfs-glossary.md)                                                | Termos especiais usados em ProjFS.

## <a name="additional-resources"></a>Recursos adicionais

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Um provedor de ProjFS de exemplo que projeta o registro do Windows no sistema de arquivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->
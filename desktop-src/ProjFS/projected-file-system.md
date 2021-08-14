---
title: Windows Sistema de arquivos projetado
description: Visão geral do Windows de Arquivos Projetado (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: d5cb20b123e72ec8e031036019a16ef1bbe2b8dc4b9bb53446c8faaced4d796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792653"
---
# <a name="windows-projected-file-system-projfs"></a>Windows ProjFS (Sistema de Arquivos Projetado)

O Windows ProjFS (Sistema de Arquivos Projetado) permite que um aplicativo de modo de usuário chamado "provedor" projete dados hierárquicos de um armazenamento de dados de apoio no sistema de arquivos, fazendo com que eles apareçam como arquivos e diretórios no sistema de arquivos. Por exemplo, um provedor simples pode projetar o registro Windows no sistema de arquivos, fazendo com que as chaves e os valores do Registro apareçam como arquivos e diretórios, respectivamente. Um exemplo de um provedor mais complexo é [o VFS para Git,](https://github.com/Microsoft/VFSForGit)que é usado para virtualizar repositórios git muito grandes.

> [!NOTE]
> O ProjFS foi projetado para uso com armazenamentos de dados de backing de alta velocidade. Uma de suas metas de design é fazer com que os dados projetados apareçam como se eles estavam localmente presentes, ocultando o fato de que os dados podem ser remotos. Assim, o ProjFS não fornece: mecanismos para relatar o progresso do recall de dados; indicação do estado online versus offline de um arquivo; nem outros recursos que podem ser desejáveis ao trabalhar com armazenamentos de dados de back-back lentos. Para esses cenários, considere usar a [API de Arquivos de Nuvem](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                                                       | Descrição |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows Guia de programação do sistema de arquivos projetado](projfs-programming-guide.md)                              | Informações conceituais sobre como implementar um aplicativo de provedor ProjFS.
| [Windows Referência da API do Sistema de Arquivos Projetado](projfs-reference.md)                                          | Informações de referência para a interface de programação ProjFS.
| [Windows Glossário do Sistema de Arquivos Projetado](projfs-glossary.md)                                                | Termos especiais usados no ProjFS.

## <a name="additional-resources"></a>Recursos adicionais

| Tópico                                                                                                             | Descrição                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Um provedor ProjFS de exemplo que projeta Windows registro no sistema de arquivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->
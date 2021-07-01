---
title: Sistema de Arquivos Projetados do Windows
description: Visão geral do Sistema de Arquivos Projetado do Windows (ProjFS)
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 68f121162efdf75fb9226b41f9b3a1121bef6480
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120581"
---
# <a name="windows-projected-file-system-projfs"></a>ProjFS (Sistema de Arquivos Projetado do Windows)

O ProjFS (Sistema de Arquivos Projetado do Windows) permite que um aplicativo de modo de usuário chamado "provedor" projete dados hierárquicos de um armazenamento de dados de suporte no sistema de arquivos, fazendo com que eles apareçam como arquivos e diretórios no sistema de arquivos. Por exemplo, um provedor simples pode projetar o Registro do Windows no sistema de arquivos, fazendo com que as chaves e os valores do Registro apareçam como arquivos e diretórios, respectivamente. Um exemplo de um provedor mais complexo é [o VFS para Git,](https://github.com/Microsoft/VFSForGit)que é usado para virtualizar repositórios git muito grandes.

> [!NOTE]
> O ProjFS foi projetado para uso com armazenamentos de dados de backing de alta velocidade. Uma de suas metas de design é fazer com que os dados projetados pareçam estar localmente presentes, ocultando o fato de que os dados podem ser remotos. Assim, o ProjFS não fornece: mecanismos para relatar o progresso do recall de dados; indicação do estado online versus offline de um arquivo; nem outros recursos que podem ser desejáveis ao trabalhar com armazenamentos de dados de back-back lentos. Para esses cenários, considere usar a [API de Arquivos de Nuvem](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                                                       | Descrição |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Guia de Programação do Sistema de Arquivos Projetado do Windows](projfs-programming-guide.md)                              | Informações conceituais sobre como implementar um aplicativo de provedor ProjFS.
| [Referência da API do Sistema de Arquivos Projetado do Windows](projfs-reference.md)                                          | Informações de referência para a interface de programação ProjFS.
| [Glossário do Sistema de Arquivos Projetado do Windows](projfs-glossary.md)                                                | Termos especiais usados no ProjFS.

## <a name="additional-resources"></a>Recursos adicionais

| Tópico                                                                                                             | Descrição                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | Um provedor ProjFS de exemplo que projeta o Registro do Windows no sistema de arquivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->
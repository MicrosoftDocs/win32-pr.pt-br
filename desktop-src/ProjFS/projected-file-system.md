---
title: Windows Sistema de arquivos projetado
description: visão geral do Windows sistema de arquivos projetado (ProjFS)
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
# <a name="windows-projected-file-system-projfs"></a>Windows Sistema de arquivos projetado (ProjFS)

o sistema de arquivos Windows projetado (ProjFS) permite que um aplicativo de modo de usuário chamado de "provedor" faça o projeto de dados hierárquicos de um armazenamento de dados de backup no sistema de arquivos, fazendo com que ele apareça como arquivos e diretórios no sistema de arquivos. por exemplo, um provedor simples pode projetar o registro de Windows no sistema de arquivos, fazendo com que as chaves e os valores do registro apareçam como arquivos e diretórios, respectivamente. Um exemplo de um provedor mais complexo é o [VFS para git](https://github.com/Microsoft/VFSForGit), que é usado para virtualizar repositórios git muito grande.

> [!NOTE]
> O ProjFS foi projetado para uso com armazenamentos de dados de backup de alta velocidade. Uma de suas metas de design é fazer com que os dados projetados apareçam como se estivessem presentes localmente, ocultando o fato de que os dados podem ser remotos. Como tal, o ProjFS não fornece: mecanismos para relatar o progresso da recuperação de dados; indicação do estado online versus offline de um arquivo; nem outros recursos que podem ser desejáveis ao trabalhar com armazenamentos de dados de backup lentos. Para esses cenários, considere usar a [API de arquivos de nuvem](../cfapi/cloud-files-api-portal.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                                                       | Descrição |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [Windows Guia de programação do sistema de arquivos projetado](projfs-programming-guide.md)                              | Informações conceituais sobre como implementar um aplicativo de provedor ProjFS.
| [Windows Referência da API do sistema de arquivos projetada](projfs-reference.md)                                          | Informações de referência para a interface de programação ProjFS.
| [Windows Glossário do sistema de arquivos projetado](projfs-glossary.md)                                                | Termos especiais usados em ProjFS.

## <a name="additional-resources"></a>Recursos adicionais

| Tópico                                                                                                             | Descrição                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Exemplo de RegFS](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | um provedor de ProjFS de exemplo que projeta o Windows registro no sistema de arquivos. |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->
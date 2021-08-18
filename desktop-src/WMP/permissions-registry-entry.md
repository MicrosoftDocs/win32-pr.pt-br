---
title: Entrada do Registro de Permissões
description: Entrada do Registro de Permissões
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, permissões
- Windows Media Player,Registro
- registro, extensões de nome de arquivo
- registro, permissões
- registry,settings for Windows Media Player
- configurações do registro de extensão de nome de arquivo
- permissões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5feaae3ebf55359f664e40df26b52912d727446ad715cd552d92cc1d090ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747733"
---
# <a name="permissions-registry-entry"></a>Entrada do Registro de Permissões

Quando Windows Media Player encontrar uma extensão de nome de arquivo personalizada, ela procura uma sub-chave do Registro que corresponde à extensão. A sub-chave é descrita em Registro de Extensão de [Nome de Arquivo Configurações](file-name-extension-registry-settings.md). Uma das entradas do Registro que podem aparecer sob a sub-chave da extensão é a **entrada Permissões.**

A **entrada Permissões** especifica as ações que Windows Media Player tem permissão para executar em arquivos que têm a extensão personalizada. A **entrada Permissões** tem o seguinte formulário.



| Nome        | Tipo           | Valor                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Permissões | **REG \_ DWORD** | Um conjunto de sinalizadores, cada um concede permissão para uma ação específica. |



 

O valor da **entrada Permissões** é um **OR** bit a bit de um ou mais dos sinalizadores a seguir.



| Sinalizador (valor decimal) | Descrição                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Permissão para reprodução. Arquivos que têm a extensão de nome de arquivo registrado podem ser interpretados.                                                                                                                                                                                       |
| 2                    | Permissão para a redução de pasta. Os arquivos que têm a extensão de nome de arquivo registrado serão incluídos na playlist criada quando o usuário arrastar uma pasta que contém os arquivos e a descarta na interface do usuário do Player.                                                      |
| 4                    | Permissão para CD de mídia. Os arquivos que têm a extensão de nome de arquivo registrado serão incluídos na playlist criada quando um CD que contém os arquivos for inserido na unidade CD-ROM.                                                                                           |
| 8                    | Permissão para a biblioteca. Arquivos que têm a extensão de nome de arquivo registrado podem ser adicionados à biblioteca. Necessário para plug-ins de conversão.                                                                                                                                    |
| 16                   | Permissão para streaming HTML. Os arquivos que têm a extensão de nome de arquivo registrado serão inseridos no cache Internet Explorer quando entregues de um fluxo da Web.                                                                                                            |
| 128                  | Permissão para transcodificação. Arquivos que têm a extensão de nome de arquivo registrado podem ser transcodificados para Windows Formato de Mídia sob determinadas condições. Consulte [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Requer Windows Media Player 10 ou posterior. |



 

Quando o usuário tenta reproduzir um arquivo de mídia que tem uma extensão de nome de arquivo personalizada, Windows Media Player procura uma sub-chave do Registro que corresponde à extensão. Se nenhuma combinação for encontrada, o Player apresentará ao usuário uma caixa de diálogo de aviso que solicita ao usuário permissão para tentar reproduzir o arquivo. Se você criar arquivos de mídia digital com extensões de nome de arquivo personalizadas, poderá impedir que esse aviso apareça no computador do usuário registrando a extensão de nome de arquivo e fornecendo uma **entrada Permissões.**

A **entrada Permissões** (exceto pelo valor de sinalizador 128) é suportada pelo Windows Media Player Série 9 e posterior. O valor do sinalizador 128 é suportado pelo Windows Media Player 10 e posteriores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Registro de Extensão de Nome de Arquivo Configurações**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





---
title: Entrada de registro de permissões
description: Entrada de registro de permissões
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, permissões
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, permissões
- registro, configurações para Windows Media Player
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
# <a name="permissions-registry-entry"></a>Entrada de registro de permissões

quando Windows Media Player encontra uma extensão de nome de arquivo personalizada, ele procura uma subchave do registro que corresponda à extensão. a subchave é descrita em [Configurações do registro de extensão de nome de arquivo](file-name-extension-registry-settings.md). Uma das entradas do registro que podem aparecer na subchave da extensão é a entrada de **permissões** .

a entrada de **permissões** especifica as ações que Windows Media Player tem permissão para executar em arquivos que têm a extensão personalizada. A entrada de **permissões** tem o seguinte formato.



| Nome        | Tipo           | Valor                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Permissões | **REG \_ DWORD** | Um conjunto de sinalizadores, cada um concedendo permissão para uma ação específica. |



 

O valor da entrada **Permissions** é uma operação OR de um ou **mais dos sinalizadores** a seguir.



| Sinalizador (valor decimal) | Descrição                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Permissão para reprodução. Arquivos com a extensão de nome de arquivo registrado podem ser reproduzidos.                                                                                                                                                                                       |
| 2                    | Permissão para drop de pasta. Os arquivos com a extensão de nome de arquivo registrado serão incluídos na playlist criada quando o usuário arrastar uma pasta que contém os arquivos e o descartará na interface do usuário do Player.                                                      |
| 4                    | Permissão para CD de mídia. Os arquivos com a extensão de nome de arquivo registrado serão incluídos na playlist criada quando um CD que contém os arquivos for inserido na unidade de CD-ROM.                                                                                           |
| 8                    | Permissão para a biblioteca. Arquivos com a extensão de nome de arquivo registrado podem ser adicionados à biblioteca. Necessário para plug-ins de conversão.                                                                                                                                    |
| 16                   | Permissão para streaming HTML. Os arquivos com a extensão de nome de arquivo registrado serão inseridos no cache do Internet Explorer quando entregues de um fluxo da Web.                                                                                                            |
| 128                  | Permissão para transcodificação. arquivos com a extensão de nome de arquivo registrado podem ser transcodificados para Windows formato de mídia em determinadas condições. Consulte [IWMPTranscodePolicy:: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). requer o Windows Media Player 10 ou posterior. |



 

quando o usuário tenta reproduzir um arquivo de mídia que tem uma extensão de nome de arquivo personalizada, Windows Media Player procura uma subchave do registro que corresponda à extensão. Se nenhuma correspondência for encontrada, o Player apresentará ao usuário uma caixa de diálogo de aviso que solicita ao usuário a permissão para tentar reproduzir o arquivo. Se você criar arquivos de mídia digital com extensões de nome de arquivo personalizadas, poderá evitar que esse aviso apareça no computador do usuário registrando a extensão de nome de arquivo e fornecendo uma entrada de **permissões** .

a entrada de **permissões** (exceto para o valor de sinalizador 128) tem suporte no Windows Media Player 9 Series e posterior. o valor do sinalizador 128 tem suporte no Windows Media Player 10 e posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações de registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





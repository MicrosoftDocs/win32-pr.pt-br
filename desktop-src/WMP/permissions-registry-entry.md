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
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- permissões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007088"
---
# <a name="permissions-registry-entry"></a>Entrada de registro de permissões

Quando o Windows Media Player encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão. A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md). Uma das entradas do registro que podem aparecer na subchave da extensão é a entrada de **permissões** .

A entrada de **permissões** especifica as ações que o Windows Media Player tem permissão para executar em arquivos que têm a extensão personalizada. A entrada de **permissões** tem o seguinte formato.



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
| 128                  | Permissão para transcodificação. Arquivos com a extensão de nome de arquivo registrado podem ser transcodificados para o formato de mídia do Windows em determinadas condições. Consulte [IWMPTranscodePolicy:: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Requer o Windows Media Player 10 ou posterior. |



 

Quando o usuário tenta reproduzir um arquivo de mídia que tem uma extensão de nome de arquivo Personalizada, o Windows Media Player procura uma subchave do registro que corresponda à extensão. Se nenhuma correspondência for encontrada, o Player apresentará ao usuário uma caixa de diálogo de aviso que solicita ao usuário a permissão para tentar reproduzir o arquivo. Se você criar arquivos de mídia digital com extensões de nome de arquivo personalizadas, poderá evitar que esse aviso apareça no computador do usuário registrando a extensão de nome de arquivo e fornecendo uma entrada de **permissões** .

A entrada de **permissões** (exceto para o valor de sinalizador 128) é suportada pelo Windows Media Player 9 Series e posterior. O valor do sinalizador 128 é suportado pelo Windows Media Player 10 e posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





---
title: Extensões de dispositivo para preferências de objeto de playlist
description: Extensões de dispositivo para preferências de objeto de playlist
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player, extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, preferências de objeto de Playlist
- extensões de dispositivo, preferências de objeto de playlist
- extensões, preferências de objeto de playlist
- Objeto playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2acb01de41b753a85fee1c69e0bf015c687da04f50a10531ee5c67b0a13cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340915"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Extensões de dispositivo para preferências de objeto de playlist

como parte do processo de sincronização, o Windows Media Player 10 ou posterior copia objetos de playlist para dispositivos portáteis habilitados para MTP. o Windows Media Player 11 apresenta uma nova funcionalidade que permite que os dispositivos portáteis limitem os tipos de objetos de playlist copiados. (Windows Media Player sempre sincroniza o conteúdo da lista de reprodução conforme especificado pelas regras de sincronização. Esse recurso afeta apenas a sincronização de objetos de lista de reprodução.) Windows Media Player copia três tipos de objetos de lista de reprodução do computador para o dispositivo:

-   **Listas de reprodução comuns.** Essas são listas de reprodução visíveis no recurso de **biblioteca** do Windows Media Player. Isso inclui listas de reprodução criadas pelo usuário, listas de reprodução adicionadas à biblioteca por lojas online e listas de reprodução de exemplo instaladas com o Player. Windows Media Player copia apenas essas listas de reprodução para o dispositivo quando o usuário as seleciona para sincronização.
-   **Listas de reprodução de sincronização de estoque.** essas são listas de reprodução especiais que são instaladas com Windows Media Player e usadas somente para sincronização. essas listas de reprodução são visíveis somente no assistente de instalação do dispositivo Windows Media Player.
-   **Listas de reprodução criadas implicitamente.** Essas listas de reprodução são criadas quando o usuário arrasta e solta uma pasta de categoria, como **artista** ou **álbum**, no painel que lista os itens a serem sincronizados.

o arquivo de cabeçalho chamado wmpdevices. h, que foi atualizado para esta versão, define as estruturas e as constantes necessárias para dar suporte a Windows Media Player extensões de dispositivo.

para que um dispositivo seja reconhecido como suporte a preferências de objeto de playlist por meio do conjunto de extensões de dispositivo Windows Media Player MTP, ele deve incluir as seguintes informações no conjunto de dados DeviceInfo. (Para obter mais informações sobre esse conjunto de dados, consulte a seção 4.6.1 da especificação do MTP.)



| Campo de conjunto de          | Ordem dos campos | Tipo de dados  | Valor                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Cadeia de caracteres** | "microsoft.com/WMPPD: 11,0" |



 

A tabela a seguir fornece detalhes sobre a operação MTP para preferências de objeto de playlist.



| Item                  | Descrição                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operação        | 0x9203                                                                                                                                                                                                                                                                                          |
| Parâmetro de operação 1 | 0                                                                                                                                                                                                                                                                                               |
| Parâmetro de operação 2 | 0                                                                                                                                                                                                                                                                                               |
| Parâmetro de operação 3 | 0                                                                                                                                                                                                                                                                                               |
| Parâmetro de operação 4 | 0                                                                                                                                                                                                                                                                                               |
| Parâmetro de operação 5 | 0                                                                                                                                                                                                                                                                                               |
| Dados                  | O dispositivo retorna um valor no parâmetro de resposta 1 para indicar a preferência de sincronização de objeto de playlist.                                                                                                                                                                                      |
| Direção dos dados        | R->I                                                                                                                                                                                                                                                                                         |
| Opções de código de resposta | MTP \_ Response \_ OK (0x2001) ou código de resposta de erro válido.                                                                                                                                                                                                                                        |
| Parâmetro de resposta 1  | 0 ou 1. um valor de 0 indica que Windows Media Player deve sincronizar apenas objetos de playlist comuns. um valor de 1 indica que esse Windows Media Player deve sincronizar objetos de lista de reprodução comuns, ações e objetos de lista de reprodução de sincronização criados implicitamente, que é o comportamento padrão. |
| Parâmetro de resposta 2  | 0                                                                                                                                                                                                                                                                                               |
| Parâmetro de resposta 3  | 0                                                                                                                                                                                                                                                                                               |
| Parâmetro de resposta 4  | 0                                                                                                                                                                                                                                                                                               |
| Parâmetro de resposta 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

A implementação desse recurso é opcional para dispositivos portáteis. o Windows Media Player sincroniza objetos de lista de reprodução comuns, objetos de playlist de sincronização de estoque e objetos de playlist criados implicitamente por padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





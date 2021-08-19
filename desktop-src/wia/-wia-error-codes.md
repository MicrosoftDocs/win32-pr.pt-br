---
description: 'Windows As funções e métodos de aquisição de imagem (WIA) podem retornar códigos de erro da seguinte lista: erro CodeMeaningCodeWIA \_ erro \_ BUSYThe dispositivo está ocupado.'
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Códigos de erro (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c782ae449a52ae0ff2b64f124609a3142f1dd457d74bdb82333502ef1868ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670269"
---
# <a name="error-codes-wia"></a>Códigos de erro (WIA)

Windows As funções e métodos de aquisição de imagem (WIA) podem retornar códigos de erro da lista a seguir: 

| Código do Erro                                      | Significado                                                                                                                                                                                                                             | Código       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| \_erro WIA \_ ocupado                                | O dispositivo está ocupado. Feche todos os aplicativos que estão usando este dispositivo ou aguarde a conclusão e tente novamente.                                                                                                                          | 0x80210006 |
| \_tampa de erro WIA \_ \_ aberta                         | Uma ou mais tampas do dispositivo estão abertas.                                                                                                                                                                                          | 0x80210016 |
| \_comunicação do \_ dispositivo de erro WIA \_               | Falha na comunicação com o dispositivo WIA. Verifique se o dispositivo está ligado e conectado ao PC. Se o problema persistir, desconecte e reconecte o dispositivo.                                                            | 0x8021000A |
| \_dispositivo de erro WIA \_ \_ bloqueado                      | O dispositivo está bloqueado. Feche todos os aplicativos que estão usando este dispositivo ou aguarde a conclusão e tente novamente.                                                                                                                        | 0x8021000D |
| \_ \_ exceção de erro WIA \_ no \_ Driver               | O driver de dispositivo lançou uma exceção.                                                                                                                                                                                               | 0x8021000E |
| erro \_ geral de erro WIA \_ \_                      | Ocorreu um erro desconhecido no dispositivo WIA.                                                                                                                                                                                  | 0x80210001 |
| erro WIA de \_ \_ configuração de hardware incorreto \_ \_        | Há uma configuração incorreta no dispositivo WIA.                                                                                                                                                                                    | 0x8021000C |
| \_comando de erro WIA \_ inválido \_                    | O dispositivo não dá suporte a este comando.                                                                                                                                                                                            | 0x8021000B |
| \_resposta de \_ \_ Driver inválido de erro \_ WIA           | A resposta do driver é inválida.                                                                                                                                                                                            | 0x8021000F |
| \_item de erro WIA \_ \_ excluído                       | O dispositivo WIA foi excluído. Ele não está mais disponível.                                                                                                                                                                               | 0x80210009 |
| \_lâmpada de erro WIA \_ \_ desativada                           | A lâmpada do verificador está desligada.                                                                                                                                                                                                          | 0x80210017 |
| \_erro WIA \_ máximo \_ do \_ contador de endossador de impressora \_ | Um trabalho de verificação foi interrompido porque um item imprimível/endossador atingiu o valor máximo válido para o \_ \_ contador de endossador de impressora IPS WIA \_ \_ e foi redefinido como 0. esse recurso está disponível com Windows 8 e versões posteriores do Windows. | 0x80210021 |
| \_ \_ vários \_ feeds de erro WIA                         | Ocorreu um erro de verificação devido a uma condição de feed de várias páginas. esse recurso está disponível com Windows 8 e versões posteriores do Windows.                                                                                            | 0x80210020 |
| \_erro WIA \_ offline                             | O dispositivo está offline. Verifique se o dispositivo está ligado e conectado ao PC.                                                                                                                                                  | 0x80210005 |
| o \_ documento de erro WIA \_ \_ está vazio                        | Não há documentos no alimentador de documentos.                                                                                                                                                                                      | 0x80210003 |
| \_ \_ emperramento de papel WIA \_                          | O papel está emperrado no alimentador de documentos do scanner.                                                                                                                                                                                   | 0x80210002 |
| \_problema de \_ papel de erro WIA \_                      | Ocorreu um problema não especificado com o alimentador de documentos do scanner.                                                                                                                                                                 | 0x80210004 |
| erro WIA em \_ \_ aquecimento \_                         | O dispositivo está se aquecendo.                                                                                                                                                                                                           | 0x80210007 |
| \_ \_ intervenção do usuário de erro WIA \_                  | Há um problema com o dispositivo WIA. Verifique se o dispositivo está ligado, online e se todos os cabos estão conectados corretamente.                                                                                                      | 0x80210008 |
| WIA \_ S \_ nenhum \_ dispositivo \_ disponível                   | Nenhum dispositivo de scanner foi encontrado. Verifique se o dispositivo está online, conectado ao PC e tem o driver correto instalado no PC.                                                                                                   | 0x80210015 |



 

 

 




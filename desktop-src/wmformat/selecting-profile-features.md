---
title: Selecionando recursos de perfil
description: Selecionando recursos de perfil
ms.assetid: 5e09000d-1417-43aa-9e9c-0aff536d52b7
keywords:
- perfis, seleção de recursos
- perfis, selecionando recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769b10387bb4fb660c31678b406090cfc7e42743
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765256"
---
# <a name="selecting-profile-features"></a>Selecionando recursos de perfil

A tabela a seguir lista os recursos de perfil e descreve quando você ou não deseja usá-los.



| Recurso                            | Quando usar                                                                                                                                                                                                                                                                                                                | Quando não usar                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exclusão mútua por taxa de bits (MBR) | O arquivo será transmitido para um público com velocidades de conexão que variam de usuário para usuário (por exemplo, arquivos entregues pela Internet).                                                                                                                                                                              | O arquivo não será transmitido em uma rede. O arquivo será transmitido em uma rede com uma largura de banda disponível consistentemente confiável (por exemplo, arquivos entregues em uma rede local corporativa).<br/>                                                              |
| Exclusão mútua por idioma       | O arquivo contém fluxos que duplicam os mesmos dados em idiomas diferentes. (Por exemplo, um filme apelidada em várias linguagens teria a trilha sonora codificada como fluxos mutuamente exclusivos.)                                                                                                                         | O arquivo contém apenas fluxos em uma única linguagem. Se o arquivo contiver apenas fluxos que devem ser alterados para idiomas individuais, pode ser mais simples criar um novo arquivo para cada idioma (por exemplo, para um filme de treinamento com muito texto no fluxo de vídeo).<br/> |
| Exclusão mútua por apresentação   | Você deseja fornecer vídeo em mais de uma taxa de proporção. Por exemplo, um arquivo pode conter o mesmo vídeo formatado para televisão e para o formato original Theatrical Wide-Screen.                                                                                                                                     | Há apenas uma versão de cada fluxo de vídeo.                                                                                                                                                                                                                                    |
| Compartilhamento de largura de banda                  | O arquivo será transmitido e terá dois ou mais fluxos que, quando combinados, usam largura de banda menos disponível do que os valores de taxa de bits de ambos os fluxos adicionados juntos. Como a taxa de bits de um fluxo é essencialmente a largura de banda máxima necessária para o fluxo, alguns fluxos podem ter alguns períodos de transferência de dados mais baixa. | O arquivo não será transmitido em uma rede. Todos os fluxos têm taxas de bits consistentes.<br/>                                                                                                                                                                                     |
| Priorização de fluxo              | O arquivo será transmitido e alguns fluxos serão mais importantes do que outros.                                                                                                                                                                                                                                                 | O arquivo não será transmitido em uma rede. Todos os fluxos são de mesma importância.<br/>                                                                                                                                                                                       |
| Extensões de unidade de dados               | Há informações importantes relacionadas aos exemplos em um fluxo que devem ser mantidos com os exemplos.                                                                                                                                                                                                                      | O arquivo destina-se à entrega por meio de uma largura de banda restrita. Nesse caso, as extensões de unidade de dados podem usar muita sobrecarga.                                                                                                                                                    |



 

Também é importante considerar os recursos de codec que você deseja usar com o arquivo ao criar um perfil. Para obter mais informações, consulte [recursos de codec](codec-features.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Criando perfis**](designing-profiles.md)
</dt> </dl>

 

 






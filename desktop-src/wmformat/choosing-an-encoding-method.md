---
title: Escolhendo um método de codificação
description: Escolhendo um método de codificação
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- perfis, escolhendo métodos de codificação
- perfis, métodos de codificação
- codecs, escolhendo métodos de codificação
- codecs, métodos de codificação
- perfis, selecionando métodos de codificação
- codecs, selecionando métodos de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763475"
---
# <a name="choosing-an-encoding-method"></a>Escolhendo um método de codificação

Alguns codecs, como o codec do Windows Media Video 9, dão suporte a vários métodos de codificação. O método de codificação que você escolher para um fluxo dependerá de como o fluxo será entregue. A tabela a seguir descreve quando usar os vários métodos de codificação.



| Método de codificação                | Descrição                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 – passar taxa de bits constante (CBR) | A única opção para transmissão ao vivo. Codifica para uma taxa de bits previsível e fornece a qualidade mais baixa de todos os métodos de codificação.                                                                    |
| 2-passar CBR                     | Use para arquivos que serão transmitidos em uma rede para um leitor de cliente, mas que não são transmitidos de uma fonte dinâmica. Codifica para uma taxa de bits previsível, mas com qualidade melhor do que 1-passar CBR. |
| 1 – passar taxa de bits variável (VBR) | Use quando precisar especificar a qualidade da saída codificada. Fornece a qualidade mais consistente de todos os métodos de codificação. Use somente para arquivos locais ou para download.                        |
| 2-passar VBR – irrestrito     | Use quando precisar especificar uma largura de banda, mas flutuações em volta da largura de banda especificada são aceitáveis. Somente para arquivos locais ou somente para download.                                                    |
| 2-passar VBR – restrito       | Use sob as mesmas circunstâncias sem restrição, mas quando você precisar especificar uma taxa de bits de tempo máxima. Somente para arquivos locais ou somente para download.                                                |



 

A tabela a seguir lista os métodos de codificação que são suportados pelos codecs fornecidos com o Windows Media Format SDK.



| Codec                                  | CBR | 2-passar CBR | BITS | 2-passar VBR |
|----------------------------------------|-----|------------|-----|------------|
| Vídeo do Windows Media 9                  | X   | X          | X   | X          |
| Windows Media Audio 9 e posterior        | X   | X          | X   | X          |
| Tela do Windows Media Video 9           | X   |            | X   |            |
| Voz do Windows Media Audio 9            | X   |            |     |            |
| Windows Media Audio Professional       | X   | X          | X   | X          |
| Windows Media Audio sem perdas           |     |            | X   |            |
| Imagem do Windows Media Video 9 e posterior  | X   |            | X   |            |
| Perfil avançado do Windows Media Video 9 | X   | X          | X   | X          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando perfis**](designing-profiles.md)
</dt> <dt>

[**Codificação de taxa de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codificação de duas passagens**](two-pass-encoding.md)
</dt> <dt>

[**Codificação de taxa de bits variável (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 





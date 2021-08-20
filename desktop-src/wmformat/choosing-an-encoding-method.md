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
ms.openlocfilehash: a87a780798885e86b515a8d111797af304a58f13c962ecab7f7862dfb1790411
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656126"
---
# <a name="choosing-an-encoding-method"></a>Escolhendo um método de codificação

alguns codecs, como o codec Windows Media Video 9, dão suporte a vários métodos de codificação. O método de codificação que você escolher para um fluxo dependerá de como o fluxo será entregue. A tabela a seguir descreve quando usar os vários métodos de codificação.



| Método de codificação                | Descrição                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 – passar taxa de bits constante (CBR) | A única opção para transmissão ao vivo. Codifica para uma taxa de bits previsível e fornece a qualidade mais baixa de todos os métodos de codificação.                                                                    |
| 2-passar CBR                     | Use para arquivos que serão transmitidos em uma rede para um leitor de cliente, mas que não são transmitidos de uma fonte dinâmica. Codifica para uma taxa de bits previsível, mas com qualidade melhor do que 1-passar CBR. |
| 1 – passar taxa de bits variável (VBR) | Use quando precisar especificar a qualidade da saída codificada. Fornece a qualidade mais consistente de todos os métodos de codificação. Use somente para arquivos locais ou para download.                        |
| 2-passar VBR – irrestrito     | Use quando precisar especificar uma largura de banda, mas flutuações em volta da largura de banda especificada são aceitáveis. Somente para arquivos locais ou somente para download.                                                    |
| 2-passar VBR – restrito       | Use sob as mesmas circunstâncias sem restrição, mas quando você precisar especificar uma taxa de bits de tempo máxima. Somente para arquivos locais ou somente para download.                                                |



 

a tabela a seguir lista os métodos de codificação que são suportados pelos codecs fornecidos com o SDK do formato de mídia Windows.



| Codec                                  | CBR | 2-passar CBR | BITS | 2-passar VBR |
|----------------------------------------|-----|------------|-----|------------|
| Windows Vídeo de mídia 9                  | X   | X          | X   | X          |
| Windows Áudio de mídia 9 e posterior        | X   | X          | X   | X          |
| Windows Tela de vídeo de mídia 9           | X   |            | X   |            |
| Windows Voz de áudio de mídia 9            | X   |            |     |            |
| Windows Professional de áudio de mídia       | X   | X          | X   | X          |
| Windows Mídia sem perdas de áudio           |     |            | X   |            |
| Windows Imagem de vídeo de mídia 9 e posterior  | X   |            | X   |            |
| Windows Perfil avançado de vídeo de mídia 9 | X   | X          | X   | X          |



 

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

 

 





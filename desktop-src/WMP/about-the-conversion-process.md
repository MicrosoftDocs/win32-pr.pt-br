---
title: Sobre o processo de conversão
description: Sobre o processo de conversão
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player, processo de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007129"
---
# <a name="about-the-conversion-process"></a>Sobre o processo de conversão

Depois que o Windows Media Player criar uma instância do plug-in de conversão, o processo continuará da seguinte maneira:

1.  O Player chama [IWMPConvert:: converterfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).
2.  O plug-in converte o arquivo fornecido no parâmetro *bstrInputFile* em um formato ASF.
3.  Se a conversão falhar por algum motivo, o plug-in retornará um código de falha apropriado e o processo será interrompido.
4.  Se a conversão for realizada com sucesso, o plug-in colocará o arquivo convertido na pasta fornecida no parâmetro *bstrDestinationFolder* e retornará o caminho totalmente qualificado para o arquivo convertido por meio do parâmetro *pbstrOutputFile* .
5.  O plug-in retorna um código de êxito do **converterfile**.
6.  O Player copia o arquivo convertido em uma pasta na hierarquia de pastas de músicas do usuário. Exatamente para onde o Player copia o arquivo depende do conteúdo. Como parte desse processo, o player pode renomear o arquivo.
7.  O Player copia o arquivo original (não convertido) para uma pasta na hierarquia de pastas de músicas do usuário. Como parte desse processo, o player pode renomear o arquivo. Essa é a cópia do arquivo que o Player usa quando o usuário sincroniza o conteúdo do computador para um dispositivo que requer o formato de arquivo original. Esse arquivo é chamado de *arquivo de sombra*.
8.  O Player adiciona informações sobre o arquivo convertido à biblioteca. Isso inclui a definição do valor do atributo **ShadowFilePath** para o novo local onde o arquivo de sombra é salvo.

Se você precisar trabalhar com o arquivo convertido, poderá consultar a biblioteca para recuperar o conteúdo usando os atributos **ContentDistributor** e **WM/UniqueFileIdentifier** . Se você precisar trabalhar com o arquivo de sombra, ainda deverá recuperar o objeto de **mídia** para o arquivo convertido e, em seguida, consultar o atributo **ShadowFilePath** . Consulte [adicionando metadados a arquivos convertidos](adding-metadata-to-converted-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre plug-ins de conversão**](about-conversion-plug-ins.md)
</dt> <dt>

[**Adicionando metadados a arquivos convertidos**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Lendo valores de atributo**](reading-attribute-values.md)
</dt> <dt>

[**Atributo ShadowFilePath**](shadowfilepath-attribute.md)
</dt> <dt>

[**Atributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Atributo WM/UniqueFileIdentifier**](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 





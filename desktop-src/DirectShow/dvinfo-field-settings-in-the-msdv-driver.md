---
description: Configurações de campo DVINFO no driver MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Configurações de campo DVINFO no driver MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645941"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a>Configurações de campo DVINFO no driver MSDV

Esta seção descreve como o driver MSDV preenche a estrutura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

A `DVINFO` estrutura define o bloco de formato para conexões de PIN entre MSDV e outros filtros. Por padrão, o filtro de Splitter de DV é usado durante a captura de um dispositivo DV e o filtro de MUX DV é usado ao transmitir para o dispositivo. No entanto, os aplicativos podem fornecer seus próprios filtros personalizados, portanto, é útil entender como o MSDV popula o `DVINFO` bloco de formato.

A `DVINFO` estrutura contém as seguintes informações:

-   Dois pacotes de origem auxiliares de áudio (AAUX), para o primeiro e o segundo blocos de áudio.
-   Dois pacotes de controle do código-fonte AAUX para o primeiro e o segundo blocos de áudio.
-   Um pacote de origem do VAUX (vídeo auxiliar).
-   Um pacote de controle do código-fonte VAUX.

Cada quadro em um fluxo de DV contém os pacotes AAUX e VAUX. No entanto, o `DVINFO` bloco de formato é estático e é usado somente para estabelecer a conexão do PIN. Quando o driver MSDV se conecta, ele não examina nenhum dos pacotes AAUX ou VAUX no fluxo. Em vez disso, ele usa um conjunto de valores padrão, com base nas seguintes características do dispositivo DV:

-   Se o dispositivo dá suporte a um formato de consumidor (DVCR) ou a um formato profissional (DVCPRO)
-   O tipo de sinal
-   Se o formato é NTSC ou PAL. (Se o dispositivo não relatar essas informações, MSDV o padrão às configurações de NTSC)

Quando o streaming começa, é responsabilidade dos filtros do modo de usuário, como o divisor DV, examinar o conteúdo real de cada quadro DV. Como as informações podem mudar de quadro para quadro, o filtro pode precisar executar uma alteração de formato dinâmico. Por exemplo, se a taxa de áudio for alterada, o filtro poderá precisar renegociar o tipo de áudio.

Se você capturar um arquivo DV tipo-1, a `DVINFO` estrutura será gravada no arquivo como a parte do formato de fluxo (' strf '). Esses dados são obtidos diretamente do bloco de formato fornecido pelo MSDV. Como observado, o conteúdo real do fluxo pode ser diferente. É responsabilidade do aplicativo examinar os pacotes AAUX e VAUX em cada quadro.

Nos tópicos a seguir, você pode encontrar tabelas listando todos os campos usados pelo MSDV.

-   [Pacote de origem do AAUX (AS)](aaux-source--as--pack.md)
-   [Pacote de controle do código-fonte AAUX (ASC)](aaux-source-control--asc--pack.md)
-   [Pacote de origem do VAUX (VS)](vaux-source--vs--pack.md)
-   [Pacote de controle do código-fonte (VSC) VAUX](vaux-source-control--vsc--pack.md)

Ao ler essas tabelas, consulte as especificações a seguir:

-   IEC 61834
-   314M SMPTE
-   SMPTE 370

Em cada tabela, a primeira coluna fornece o código de campo, seguido pelo número de bits (entre parênteses). As colunas restantes fornecem os valores de campo. Muitos dos campos AAUX e VAUX não são relevantes para a conexão de PIN; nesse caso, MSDV define um valor fictício. O valor numérico do pacote inteiro é listado na parte inferior de cada tabela.

As observações depois de cada tabela fornecem mais informações sobre os campos selecionados. Para obter descrições completas, consulte as especificações. Além disso, alguns campos não têm o mesmo significado em SMPTE 314M/SMPTE 370 como no IEC 61834.

> [!Note]  
> Atualmente, o DirectShow não oferece suporte a formatos DVCPRO. Os valores listados para os formatos DVCPRO são definidos para uso futuro.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dados de DV no formato de arquivo AVI](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[Driver MSDV](msdv-driver.md)
</dt> </dl>

 

 




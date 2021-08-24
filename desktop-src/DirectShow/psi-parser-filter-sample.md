---
description: Exemplo de filtro do analisador PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Exemplo de filtro do analisador PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de960d36900a417212cdd34ac795b504d4ad073ccd61619ffad110d5fe125fad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747916"
---
# <a name="psi-parser-filter-sample"></a>Exemplo de filtro do analisador PSI

## <a name="description"></a>Descrição

O filtro analisador PSI recebe PSI (Informações Específicas do Programa) de um fluxo de transporte MPEG-2 e extrai informações do programa da PAT (Tabela de Associação do Programa) e pmt (tabelas de mapa do programa). Essas informações permitem que um aplicativo configure o Demultiplexer MPEG-2. O filtro dá suporte a uma interface [**personalizada, IMpeg2PsiParser**](impeg2psiparser.md), para recuperar as informações do PSI.

Esse filtro foi projetado para dispositivos MPEG-2, como IEEE 1394 câmeras MPEG-2 e dispositivos D-VHS. Confira [Driver MSTape](mstape-driver.md) para obter mais informações. As fontes de transmissão de tv digital devem usar um filtro TIF para obter informações do programa.

## <a name="usage"></a>Uso

Você pode testar o filtro analisador PSI no GraphEdit da seguinte forma:

1.  Iniciar GraphEdit.
2.  Insira uma fonte de transporte MPEG-2. Os dispositivos MPEG-2 e D-VHS aparecem como "Dispositivo de Subunidade de Fita AV/C da Microsoft" na categoria Fontes de Captura de Vídeo.
3.  Conexão o filtro de origem para o filtro Demultiplexer MPEG-2.
4.  Use a página de propriedades no demux para criar um pino de saída com um tipo de mídia "MPEG-2 PSI". Esse pino fornecerá as seções PAT e PMT.
5.  Use a página de propriedades demux para mapear o PID 0x00 para o pino de saída. De definir o tipo de conteúdo como "Seções MPEG2 PSI".
6.  Conexão pino de saída demux para o Analisador PSI, conforme mostrado no diagrama a seguir.

    ![grafo de filtro do analisador psi](images/psi-parser.png)

7.  Execute o grafo para alimentar dados PSI para o filtro analisador PSI. À medida que o filtro decodifica as seções pat, ele mapeia automaticamente os PIDs pmt para o mesmo pino de saída no demux, para que ele receba as seções PMT.
8.  Use a página de propriedades analisador PSI para selecionar um número de programa. A lista de fluxos elementares na página de propriedades mostrará o PID e o tipo de fluxo associado a cada fluxo elementar no programa selecionado. A página de propriedades foi projetada para reconhecer tipos de fluxo definidos em ISO/IEC 13818-1.
9.  Insira o número PID de áudio na caixa de edição **PID** de áudio e o número PID do vídeo na caixa de edição **PID** do vídeo.
10. Clique no **botão Exibir Programa.** O Analisador PSI configurará os pinos de saída no demux para corresponder às informações de fluxo do programa e renderizar os pinos.

> [!Note]  
> A página de propriedades do Analisador PSI é fornecida para facilitar o teste e para fornecer um código de exemplo que configura o Demultiplexer MPEG-2. Não é recomendável que os aplicativos usem. Os aplicativos devem configurar o demux programaticamente.

 

Para usar o filtro analisador PSI em um aplicativo, comece criando o grafo de filtro da fonte MPEG-2 para o demux MPEG-2. O código dessa etapa não é mostrado aqui, porque a configuração exata do grafo dependerá da origem.

Em seguida, crie um pino de saída no demux para os dados PSI. Mapeie 0x00 PID, que é reservado para seções PAT, para esse pino, conforme mostrado no código a seguir:


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



Para obter mais informações, [consulte Usando o Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md).

Adicione o filtro analisador PSI ao grafo e conecte-o ao pino de saída no demux. Consulte o Analisador PSI para a interface [**IMpeg2PsiParser.**](impeg2psiparser.md) Agora, execute o grafo e aguarde os eventos EC PROGRAM CHANGED, que \_ \_ sinalizam uma nova seção PAT ou PMT. Esse evento é um evento personalizado definido pelo filtro analisador PSI. Ao receber um evento EC PROGRAM CHANGED, você pode obter as informações de PSI disponíveis chamando métodos \_ \_ **IMpeg2PsiParser.** Esta seção descreve os métodos que você precisará com mais frequência.

Para obter o número de programas, use o [**método IMpeg2PsiParser::GetCountOfPrograms:**](impeg2psiparser-getcountofprograms.md)


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Para obter o número do programa para um programa específico, use o [**método IMpeg2PsiParser::GetRecordProgramNumber:**](impeg2psiparser-getrecordprogramnumber.md)


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



O número do programa é usado para obter as entradas PMT para programas individuais. Para obter o número de fluxos elementares em um programa, use o [**método GetCountOfElementaryStreams:**](impeg2psiparser-getcountofelementarystreams.md)


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Para cada fluxo elementar, o método [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) retorna o PID e o [**método IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) retorna o tipo de fluxo:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



O PID e o tipo de fluxo permitem que você configure novos pinos de saída no Demultiplexer MPEG-2. Isso pode exigir algum conhecimento da origem original. Por exemplo, ISO/IEC 13818-1 define tipos de fluxo 0x80 por meio do 0xFF como "privado do usuário", mas outros padrões baseados no MPEG-2 podem atribuir outros significados a esses tipos.

O Demultiplexer MPEG-2 pode criar novos pinos e novos mapeamentos PID enquanto o grafo está em execução, mas você deve parar o grafo para conectar os pinos.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os DirectShow exemplos do SDK, instale a versão mais recente do [SDK Windows .](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este exemplo é instalado no seguinte caminho: *\[ SDK Root \]* \\ Samples Multimedia DirectShow Filters \\ \\ \\ \\ PSIParser.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Amostras](directshow-samples.md)
</dt> <dt>

[**IMpeg2PsiParser Interface**](impeg2psiparser.md)
</dt> </dl>

 

 

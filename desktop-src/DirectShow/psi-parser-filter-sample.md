---
description: Exemplo de filtro do analisador PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Exemplo de filtro do analisador PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551191"
---
# <a name="psi-parser-filter-sample"></a>Exemplo de filtro do analisador PSI

## <a name="description"></a>Description

O filtro do analisador PSI recebe informações específicas do programa (PSI) de um fluxo de transporte MPEG-2 e extrai informações do programa da PAT (tabela de associação de programa) e do pgto (tabelas de mapa do programa). Essas informações permitem que um aplicativo configure o demultiplexador MPEG-2. O filtro oferece suporte a uma interface personalizada, [**IMpeg2PsiParser**](impeg2psiparser.md), para recuperar as informações de psi.

Esse filtro foi projetado para dispositivos MPEG-2, como IEEE 1394 MPEG-2 camcorders e dispositivos D-VHS. Consulte o [Driver MSTape](mstape-driver.md) para obter mais informações. As fontes de difusão de televisão digital devem usar um filtro TIF para obter informações sobre o programa.

## <a name="usage"></a>Uso

Você pode testar o filtro do analisador PSI no GraphEdit da seguinte maneira:

1.  Inicie o GraphEdit.
2.  Insira uma fonte de transporte MPEG-2. Os dispositivos de camcorder MPEG-2 e D-VHS aparecem como "dispositivo de subunidade de fita AV/C da Microsoft" na categoria fontes de captura de vídeo.
3.  Conecte o filtro de origem ao filtro de Desmultiplexador MPEG-2.
4.  Use a página de propriedades no Demux para criar um pino de saída com um tipo de mídia "MPEG-2 PSI". Esse PIN fornecerá as seções PAT e pgto.
5.  Use a página de propriedades Demux para mapear o PID 0x00 para o pino de saída. Defina o tipo de conteúdo como "seções PSI do MPEG2".
6.  Conecte o pino de saída Demux ao analisador PSI, conforme mostrado no diagrama a seguir.

    ![Grafo de filtro do analisador psi](images/psi-parser.png)

7.  Execute o grafo para alimentar dados PSI ao filtro do analisador PSI. Como o filtro decodifica as seções PAT, ele mapeia automaticamente os PIDs de PGTO para o mesmo pino de saída no Demux, para que ele receba as seções pgto.
8.  Use a página de propriedades do analisador PSI para selecionar um número de programa. A lista de fluxos elementares na página de propriedades mostrará a PID e o tipo de fluxo associados a cada fluxo elementar no programa selecionado. A página de propriedades foi projetada para reconhecer os tipos de fluxo definidos no ISO/IEC 13818-1.
9.  Insira o número da PID de áudio na caixa de edição **pid de áudio** e o número de PID do vídeo na caixa de edição **pid do vídeo** .
10. Clique no botão **Exibir programa** . O analisador PSI configurará os Pins de saída no Demux para corresponder às informações de fluxo do programa e renderizar os Pins.

> [!Note]  
> A página de propriedades do analisador PSI é fornecida para facilitar o teste e fornecer um código de exemplo que configure o demultiplexador MPEG-2. Não é recomendável que os aplicativos usem. Os aplicativos devem configurar o Demux de forma programática.

 

Para usar o filtro do analisador PSI em um aplicativo, comece criando o grafo de filtro da origem MPEG-2 para o Demux MPEG-2. O código desta etapa não é mostrado aqui, pois a configuração exata do grafo dependerá da origem.

Em seguida, crie um PIN de saída no Demux para os dados PSI. MAP PID 0x00, que é reservado para seções PAT, para esse PIN, conforme mostrado no código a seguir:


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



Para obter mais informações, consulte [usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md).

Adicione o filtro do analisador PSI ao grafo e conecte-o ao pino de saída no Demux. Consulte o analisador PSI para a interface [**IMpeg2PsiParser**](impeg2psiparser.md) . Agora, execute o grafo e aguarde os \_ eventos de alteração do programa do EC \_ , que sinalizam uma nova seção Pat ou pgto. Esse evento é um evento personalizado definido pelo filtro do analisador PSI. Ao receber um evento de \_ alteração de programa do EC \_ , você pode obter as informações de psi disponíveis chamando métodos **IMpeg2PsiParser** . Esta seção descreve os métodos que serão necessários com mais frequência.

Para obter o número de programas, use o método [**IMpeg2PsiParser:: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Para obter o número do programa para um programa específico, use o método [**IMpeg2PsiParser:: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



O número do programa é usado para obter as entradas de PGTO para programas individuais. Para obter o número de fluxos elementares em um programa, use o método [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Para cada fluxo elementar, o método [**IMpeg2PsiParser:: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) retorna o PID e o método [**IMpeg2PsiParser:: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) retorna o tipo de fluxo:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



A PID e o tipo de fluxo permitem configurar novos PINs de saída no demultiplexador MPEG-2. Isso pode exigir algum conhecimento da fonte original. Por exemplo, o ISO/IEC 13818-1 define os tipos de fluxo 0x80 por meio de 0xFF como "particular do usuário", mas outros padrões baseados em MPEG-2 podem atribuir outros significados a esses tipos.

O demultiplexador MPEG-2 pode criar novos PINs e novos mapeamentos de PID enquanto o grafo está em execução, mas você deve parar o grafo para conectar Pins.

## <a name="downloading-the-sample"></a>Baixando o exemplo

Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do \\ \\ DirectShow \\ \\ PSIParser.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras do DirectShow](directshow-samples.md)
</dt> <dt>

[**Interface IMpeg2PsiParser**](impeg2psiparser.md)
</dt> </dl>

 

 

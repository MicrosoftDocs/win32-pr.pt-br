---
description: Especifica os atributos de um IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Enumeração RecognizerCapabilities (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 96e932b8e47f323198e1b0cc87da0df7839a593a76850c00c2c2e4d095854851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091446"
---
# <a name="recognizercapabilities-enumeration"></a>Enumeração RecognizerCapabilities

Especifica os atributos de um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ nenhum**
</dt> <dd>

Nenhum recurso especificado.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**\_DONOTCARE RC**
</dt> <dd>

Ignora todos os outros sinalizadores que estão definidos.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**\_Objeto RC**
</dt> <dd>

Dá suporte ao reconhecimento de objeto; caso contrário, o só reconhecerá o texto.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**\_FREEINPUT RC**
</dt> <dd>

Dá suporte à entrada gratuita, em que a tinta é inserida sem o uso de um guia de reconhecimento, como uma linha ou uma caixa.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**\_LINEDINPUT RC**
</dt> <dd>

Dá suporte à entrada em linha, que é semelhante à escrita em papel embutido.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**\_BOXEDINPUT RC**
</dt> <dd>

Dá suporte à entrada em caixa, em que cada caractere ou palavra é inserida em um box.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**\_CHARACTERAUTOCOMPLETIONINPUT RC**
</dt> <dd>

Dá suporte ao preenchimento automático de caracteres. Os reconhecedores que dão suporte ao preenchimento automático de caracteres exigem entrada em caixa.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**\_RIGHTANDDOWN RC**
</dt> <dd>

Dá suporte à entrada de manuscrito na ordem direita e abaixo, como em idiomas ocidentais e em alguns idiomas do leste asiático.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**\_LEFTANDDOWN RC**
</dt> <dd>

Dá suporte à entrada de manuscrito em ordem esquerda e abaixo, como em idiomas hebraico e árabe.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**\_DOWNANDLEFT RC**
</dt> <dd>

Dá suporte à entrada de manuscrito na ordem inferior e esquerda, como em alguns idiomas do leste asiático.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**\_DOWNANDRIGHT RC**
</dt> <dd>

Dá suporte à entrada de manuscrito na ordem inferior e direita, como em alguns idiomas do leste asiático.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**\_ARBITRARYANGLE RC**
</dt> <dd>

Dá suporte a texto escrito em ângulos arbitrários.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**\_Malha RC**
</dt> <dd>

Dá suporte ao retorno de um malha como uma cadeia de caracteres alternativa para resultados de reconhecimento de manuscrito.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**\_ADVISEINKCHANGE RC**
</dt> <dd>

Dá suporte à interrupção do reconhecimento em segundo plano, como quando a tinta foi alterada.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**\_STROKEREORDER RC**
</dt> <dd>

Dá suporte a essa ordem de traço, espacial e temporal, é tratada como parte da operação de reconhecimento. O [**IInkAnalyzer**](iinkanalyzer.md) não reordena os traços antes de enviar tinta para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**A versão RC é \_ personalizável**
</dt> <dd>

Dá suporte a manuscrito personalizado, onde o reconhecedor melhora o reconhecimento quando exposto ao mesmo manuscrito ao longo do tempo.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**\_PREFERSARBITRARYANGLE RC**
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) não precisa girar o manuscrito para uma orientação horizontal antes de enviar a tinta para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**\_PREFERSPARAGRAPHBREAKING RC**
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) deve enviar parágrafos inteiros de tinta para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), permitindo que o **IInkAnalysisRecognizer** faça a quebra de linha e a palavra (ou caractere).

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**\_PREFERSSEGMENTATIONRECOGNITION RC**
</dt> <dd>

Reconhece apenas uma palavra ou um caractere por operação de reconhecimento. O [**IInkAnalyzer**](iinkanalyzer.md) executa segmentação no manuscrito e envia apenas um segmento de cada vez para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração permite uma combinação de bit a bit de seus valores de membro. Use essa enumeração para localizar um reconhecedor de tinta instalado que dê suporte aos atributos necessários.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalysisRecognizer:: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 





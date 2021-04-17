---
description: Fornece acesso a reconhecedores de manuscrito para uso com a análise de tinta.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interface IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813573"
---
# <a name="iinkanalysisrecognizer-interface"></a>Interface IInkAnalysisRecognizer

Fornece acesso a reconhecedores de manuscrito para uso com a análise de tinta.

## <a name="members"></a>Membros

A interface **IInkAnalysisRecognizer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IInkAnalysisRecognizer** tem esses métodos.



| Método                                                                          | Descrição                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Recupera os recursos do reconhecedor.<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | Recupera o identificador global exclusivo (GUID) do reconhecedor.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Recupera os identificadores para as localidades às quais esse **IInkAnalysisRecognizer** dá suporte.<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Recupera o nome do reconhecedor.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Recupera os identificadores globalmente exclusivos (GUIDs) para as propriedades às quais esse **IInkAnalysisRecognizer** dá suporte.<br/> |
| [**Getvendor**](iinkanalysisrecognizer-getvendor.md)                           | Recupera o nome do fornecedor do **IInkAnalysisRecognizer**.<br/>                                                        |



 

## <a name="remarks"></a>Comentários

Um reconhecedor tem atributos e propriedades específicos que permitem que ele execute o reconhecimento. As propriedades de um reconhecedor devem ser determinadas antes que o reconhecimento possa ocorrer. Os tipos de propriedades que um reconhecedor dá suporte determinam os tipos de reconhecimento que ele pode executar. Por exemplo, se um reconhecedor não oferecer suporte a manuscritos cursivos, ele retornará resultados imprecisos quando um usuário gravar em letra cursiva.

Um reconhecedor também tem uma funcionalidade interna que gerencia automaticamente muitos aspectos do manuscrito. Por exemplo, ele determina as métricas para as linhas nas quais os traços são desenhados. Você pode retornar o número de linha de um traço, mas nunca precisa especificar como essas métricas de linha são determinadas devido à funcionalidade interna do reconhecedor.

O [**IInkAnalyzer**](iinkanalyzer.md) mantém uma lista de reconhecedores disponíveis. Para acessar essa lista, use o método do [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 


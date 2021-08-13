---
description: Fornece acesso a reconhecedores de manuscrito para uso com análise de tinta.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interface IInkAnalysisRecognizer (IACom.h)
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
ms.openlocfilehash: d0736288658c57c1cfd346b8337f91353638b8326ed1d0b29687c812db72efba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350876"
---
# <a name="iinkanalysisrecognizer-interface"></a>Interface IInkAnalysisRecognizer

Fornece acesso a reconhecedores de manuscrito para uso com análise de tinta.

## <a name="members"></a>Membros

A interface **IInkAnalysisRecognizer** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalysisRecognizer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IInkAnalysisRecognizer** tem esses métodos.



| Método                                                                          | Descrição                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Recupera os recursos do reconhecedor.<br/>                                                                       |
| [**Getguid**](iinkanalysisrecognizer-getguid.md)                               | Recupera o GUID (identificador global exclusivo) do reconhecedor.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Recupera os identificadores das localidades compatíveis com **esse IInkAnalysisRecognizer.**<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Recupera o nome do reconhecedor.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Recupera os GUIDs (identificadores globalmente exclusivos) para as propriedades que esse **IInkAnalysisRecognizer** dá suporte.<br/> |
| [**GetVendor**](iinkanalysisrecognizer-getvendor.md)                           | Recupera o nome do fornecedor do **IInkAnalysisRecognizer.**<br/>                                                        |



 

## <a name="remarks"></a>Comentários

Um reconhecedor tem atributos e propriedades específicos que permitem que ele execute o reconhecimento. As propriedades de um reconhecedor devem ser determinadas antes que o reconhecimento possa ocorrer. Os tipos de propriedades aos quais um reconhecedor dá suporte determinam os tipos de reconhecimento que ele pode executar. Por exemplo, se um reconhecedor não dá suporte à manuscrito cursivo, ele retorna resultados imprecisos quando um usuário grava em cursiva.

Um reconhecedor também tem funcionalidades criadas que gerenciam automaticamente muitos aspectos do manuscrito. Por exemplo, ele determina as métricas para as linhas nas quais os traços são desenhados. Você pode retornar o número de linha de um traço, mas nunca precisa especificar como essas métricas de linha são determinadas devido à funcionalidade do reconhecedor.

O [**IInkAnalyzer**](iinkanalyzer.md) mantém uma lista de reconhecedores disponíveis. Para acessar essa lista, use o [**método IInkAnalyzer::GetInkAnalysisRecognizersByPriority.**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 


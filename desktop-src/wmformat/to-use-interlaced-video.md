---
title: Para usar vídeo entrelaçado
description: Para usar vídeo entrelaçado
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- SDK do Windows Media Format, vídeo entrelaçado
- SDK do Windows Media Format, codificação de vídeo entrelaçada
- SDK de formato de mídia do Windows, vídeo entrelaçado de codificação
- SDK do Windows Media Format, decodificando vídeo entrelaçado
- Windows Media Format SDK, ordem de campo
- ASF (Advanced Systems Format), vídeo entrelaçado
- ASF (formato de sistemas avançados), vídeo entrelaçado
- ASF (Advanced Systems Format), codificação de vídeo entrelaçado
- ASF (formato de sistemas avançados), codificação de vídeo entrelaçado
- ASF (Advanced Systems Format), vídeo entrelaçado de codificação
- ASF (formato de sistemas avançados), vídeo entrelaçado de codificação
- Formato de sistema avançado (ASF), decodificação de vídeo entrelaçado
- ASF (formato de sistemas avançados), decodificando vídeo entrelaçado
- Formato de sistema avançado (ASF), ordem de campo
- ASF (formato de sistemas avançados), ordem de campo
- vídeo entrelaçado, sobre
- vídeo entrelaçado, codificação
- vídeo entrelaçado, decodificação
- vídeo entrelaçado, ordem de campo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823568"
---
# <a name="to-use-interlaced-video"></a>Para usar vídeo entrelaçado

Há dois tipos básicos de codificação de vídeo: progressivo e entrelaçado. Na codificação progressiva, cada quadro é uma representação codificada de um quadro de vídeo. Na codificação entrelaçada, cada quadro é uma representação codificada de todas as linhas pares de pixels no vídeo ou todas as linhas ímpares. Cada quadro entrelaçado é chamado de *campo*, portanto, há campos ímpares e até mesmo campos. Uma exibição entrelaçada (como uma televisão) renderiza os campos um de cada vez, alternando campos. Uma exibição progressiva renderiza quadros todos de uma vez.

O codec de perfil avançado do Windows Media Video 9 fornece suporte para manter o entrelaçamento em fluxos compactados.

## <a name="when-to-use-interlaced-video"></a>Quando usar vídeo entrelaçado

O vídeo entrelaçado de codificação só é útil quando o conteúdo é exibido em um dispositivo entrelaçado. O conteúdo que deve ser exibido em uma televisão (por meio de um conjunto de decodificador ou outro dispositivo) pode precisar ser entrelaçado. O conteúdo que se destina a ser exibido exclusivamente em uma exibição do computador não deve ser codificado como entrelaçado.

Para codificar vídeo entrelaçado como vídeo progressivo, você deve definir as configurações de entrada. Para obter mais informações, consulte [para desentrelaçar vídeo](to-deinterlace-video.md).

## <a name="field-order"></a>Ordem de Campos

A maioria das fontes de vídeo entrelaçado, como cartões de captura de vídeo, fornece amostras de vídeo que incluem ambos os campos intercalados entre si. O resultado é como um quadro de vídeo completo, exceto que as linhas ímpares e pares são um pouco deslocadas no tempo. Não há um padrão universal no qual o campo no exemplo de vídeo intercalado ocorre primeiro no tempo.

Você deve permitir que os usuários especifiquem a ordem dos campos ao passar amostras entrelaçadas para seu aplicativo.

## <a name="encoding-interlaced-video"></a>Vídeo entrelaçado de codificação

Para usar a codificação entrelaçada, execute as seguintes etapas:

1.  Configure o fluxo de vídeo no perfil para usar a extensão de unidade de dados do tipo de conteúdo chamando o método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) . O GUID de extensão de exemplo para a extensão de tipo de conteúdo é WM \_ SampleExtensionsGUID \_ ContentType.
2.  Defina o fluxo no perfil e configure o gravador com o perfil como normal.
3.  Antes de passar amostras entrelaçadas para o gravador, chame o método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para definir a \_ configuração de entrada g wszInterlacedCoding como **true**.
4.  Para cada amostra entrelaçada que você passa para o gravador, chame o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para definir o tipo de conteúdo. Os valores de tipo de conteúdo são combinações dos sinalizadores na tabela a seguir.



| Sinalizador                         | Descrição                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ CT \_ entrelaçado           | Sempre defina esse sinalizador ao codificar conteúdo entrelaçado. Se você usar esse sinalizador sem definir um sinalizador de ordem de campo ( \_ primeiro, o campo do WM CT \_ \_ na parte \_ \_ superior ou \_ \_ o primeiro campo do WM CT \_ ) o codec assumirá que o campo superior é primeiro. Se o codec usar a ordem de campo incorreta, não deverá haver nenhum impacto na qualidade da imagem, mas a eficiência da codificação será afetada. |
| \_primeiro campo do WM CT na \_ parte inferior \_ \_ | Quando combinado com o sinalizador do WM \_ CT \_ entrelaçado, esse sinalizador indica que o campo inferior (o campo que começa com a segunda linha no exemplo) ocorre primeiro no tempo.                                                                                                                                                                                          |
| primeiro campo do WM \_ CT \_ principal \_ \_    | Quando combinado com o sinalizador do WM \_ CT \_ entrelaçado, esse sinalizador indica que o campo superior (o campo que começa com a primeira linha no exemplo) ocorre primeiro no tempo.                                                                                                                                                                                              |
| \_ \_ \_ primeiro campo de repetição do WM CT \_ | Indica que o primeiro campo no exemplo deve ser repetido na reprodução. Esse sinalizador é usado para vídeo criado a partir do filme pelo processo de telecineon. Se nenhum sinalizador de ordem de campo for definido em conjunto com esse sinalizador, presume-se que o campo superior ocorra primeiro no tempo.<br/>                                                                             |



 

> [!Note]  
> Se o sinalizador do WM \_ CT \_ entrelaçado não estiver definido, o exemplo será considerado para conter um quadro de vídeo progressivo.

 

## <a name="decoding-interlaced-video"></a>Decodificando vídeo entrelaçado

Ao decodificar vídeo entrelaçado, você deve definir a configuração g \_ wszAllowInterlacedOutput como **true** usando o método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . Caso contrário, o codec fornecerá quadros progressivos.

A extensão de unidade de dados de tipo de conteúdo é mantida nos exemplos de saída. Você deve passar a orientação do campo para o dispositivo de renderização para garantir a reprodução correta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> </dl>

 

 






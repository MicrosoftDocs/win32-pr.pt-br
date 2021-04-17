---
description: Especifica se o coletor de mídia ASF ajusta automaticamente a taxa de bits.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Propriedade MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763264"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>\_Propriedade MFPKEY ASFMEDIASINK \_ autoadjust \_ taxa de bits

Especifica se o coletor de mídia ASF ajusta automaticamente a taxa de bits.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL de variante \_**

BOOL do VT \_

**boolVal**



## <a name="remarks"></a>Comentários

Se o valor dessa propriedade for VARIANT \_ true, o coletor de mídia ASF ajustará automaticamente a taxa de bits do conteúdo ASF em resposta às características dos fluxos que estão sendo multiplexados.

Essa propriedade afeta a forma como o coletor de mídia ASF se comporta quando um fluxo estoura os parâmetros de "Bucket de vazamentos" do coletor:



| Valor              | Comportamento                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANTE \_ true**  | O coletor de mídia ASF ajusta automaticamente a taxa de bits do conteúdo ASF em resposta às características dos fluxos que estão sendo multiplexados. |
| **VARIANTE \_ falso** | O coletor de mídia ASF usa o valor de taxa de bits de fluxo fornecido pelo aplicativo.                                                                |



 

O valor padrão é **Variant \_ false**.

Defina essa propriedade ao configurar o coletor de mídia ASF. O uso depende de qual função você chama para criar o coletor de mídia ASF:

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): consulta o ponteiro [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para a interface **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) no ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado no parâmetro *pContentInfo* .

Definir essa propriedade como VARIANT \_ true faz com que o coletor de mídia ASF defina o sinalizador de **taxa de bits do MFASF \_ multiplexador \_ \_ AutoAjuste** no Multiplexador de ASF. Consulte [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).

Para obter mais informações sobre o conceito de Bucket de vazamento, consulte o tópico "o modelo de buffer de buckets de vazamentos" na documentação do Windows Media Format SDK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 





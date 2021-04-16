---
description: Especifica a configuração do alto-falante no computador cliente.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: Propriedade MFPKEY_WMADEC_SPKRCFG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505699"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>\_Propriedade MFPKEY WMADEC \_ SPKRCFG

Especifica a configuração do alto-falante no computador cliente.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACSpeakerConfig

## <a name="data-type"></a>Tipo de Dados

**\_UI4 VT**

## <a name="default-value"></a>Valor padrão

Nenhuma configuração de alto-falante específica é assumida.

## <a name="remarks"></a>Comentários

Você deve definir esse valor como uma das constantes ou valores na tabela a seguir. As constantes são definidas no Microsoft DirectSound e são listadas aqui para sua conveniência. Para resolver esses nomes de constantes para seu compilador, você deve incluir dsound. h.



| Constante             | Valor      | Descrição                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ directout | 0x00000000 | O áudio é transmitido diretamente, sem ser configurado para os alto-falantes. |
| \_fone de ouvido DSSPEAKER | 0x00000001 | O computador cliente está equipado com fones de ouvido.                             |
| DSSPEAKER \_ mono      | 0x00000002 | O computador cliente está equipado com um monoaural palestrante.                    |
| DSSPEAKER \_ Quad      | 0x00000003 | O computador cliente está equipado com alto-falantes Quadraphonic.                  |
| estéreo de DSSPEAKER \_    | 0x00000004 | O computador cliente está equipado com alto-falantes estéreo.                        |
| \_surround DSSPEAKER  | 0x00000005 | O computador cliente está equipado com alto-falantes surround-sound.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | O computador cliente é equipado com cinco alto-falantes e um subwoofer.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | O computador cliente está equipado com sete palestrantes e um subwoofer.         |



 

O valor definido para essa propriedade determina os formatos de saída enumerados pelo codec para áudio multicanal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





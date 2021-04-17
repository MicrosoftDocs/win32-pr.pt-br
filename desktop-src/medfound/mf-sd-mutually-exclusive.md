---
description: Especifica se um fluxo é mutuamente exclusivo com outros fluxos do mesmo tipo.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Atributo MF_SD_MUTUALLY_EXCLUSIVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812041"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>\_Atributo de SD do MF \_ \_

Especifica se um fluxo é mutuamente exclusivo com outros fluxos do mesmo tipo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Comentários

Se esse atributo for **true** (diferente de zero), o fluxo será mutuamente exclusivo com outros fluxos do mesmo tipo, como áudio ou vídeo, dentro da mesma apresentação. Por exemplo, se um arquivo AVI contiver vários fluxos de áudio, eles serão marcados como mutuamente exclusivos, porque apenas um fluxo de áudio deve ser reproduzido ao mesmo tempo.

O valor padrão é **false**.

> [!Note]  
> Esse atributo não é usado para arquivos ASF (Advanced Systems Format), que têm uma maneira mais sofisticada de representar critérios de exclusão mútua. Para obter mais informações, consulte [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).

 

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> </dl>

 

 





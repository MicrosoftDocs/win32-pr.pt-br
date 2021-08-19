---
title: Propriedade IMsRdpClientAdvancedSettings7 AudioQualityMode
description: Especifica ou recupera um valor que indica a configuração do modo de qualidade de áudio para áudio Redirecionado. Por padrão, é definido como 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AudioQualityMode
- Propriedade AudioQualityMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade AudioQualityMode
- Propriedade AudioQualityMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1635c2ed01144a640b624a014959a4847ae5f746502267444d958a20b959eef9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001304"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>Propriedade IMsRdpClientAdvancedSettings7:: AudioQualityMode

Especifica ou recupera um valor que indica a configuração do modo de qualidade de áudio para áudio Redirecionado. Por padrão, é definido como 0.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a>Valor da propriedade

Um valor que especifica o modo de qualidade de áudio.

Os valores possíveis são:

<dt>

0
</dt> <dd>

Qualidade de áudio dinâmica. Essa é a configuração de qualidade de áudio padrão. O servidor ajusta dinamicamente a qualidade de saída de áudio em resposta às condições de rede e aos recursos de cliente e servidor.

</dd> <dt>

1
</dt> <dd>

Qualidade de áudio médio. O servidor usa um formato fixo, mas compactado, para saída de áudio.

</dd> <dt>

2
</dt> <dd>

Alta qualidade de áudio. O servidor fornece a saída de áudio no formato PCM descompactado com menor sobrecarga de processamento para latência.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 






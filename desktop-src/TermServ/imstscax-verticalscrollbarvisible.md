---
title: Propriedade VerticalScrollBarVisible de IMsTscAx
description: Indica se o controle exibe uma barra de rolagem vertical.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsTscAx
- Interface IMsTscAx Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient
- Interface IMsRdpClient Serviços de Área de Trabalho Remota propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota interface , IMsRdpClient2
- Interface IMsRdpClient2 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient3
- Interface IMsRdpClient3 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
- Propriedade VerticalScrollBarVisible Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , propriedade VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b09cf6c50c4724cc7374163998af7b7bab77d61f4c16177fedddcc9b1e8de055
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125256"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a>Propriedade IMsTscAx::VerticalScrollBarVisible

Indica se o controle exibe uma barra de rolagem vertical.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a>Valor da propriedade

O valor desse parâmetro será **TRUE se** a barra de rolagem vertical estiver visível, caso contrário, **FALSE.**

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

O controle exibirá automaticamente uma barra de rolagem vertical se a altura do controle atual for menor que a altura da área de trabalho.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsTscAx é definido como \_ 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 






---
title: Propriedade IMsTscAx HorizontalScrollBarVisible
description: Indica se o controle exibiu uma barra de rolagem horizontal.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade HorizontalScrollBarVisible
- Propriedade HorizontalScrollBarVisible Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade HorizontalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009294"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a>Propriedade IMsTscAx:: HorizontalScrollBarVisible

Indica se o controle exibiu uma barra de rolagem horizontal.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a>Valor da propriedade

O valor desse parâmetro será **true** se a barra de rolagem horizontal estiver visível e **false** caso contrário.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

O controle exibirá automaticamente uma barra de rolagem horizontal se a largura do controle for menor que a largura da área de trabalho.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
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

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 






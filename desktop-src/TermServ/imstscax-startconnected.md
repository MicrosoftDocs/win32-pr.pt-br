---
title: Propriedade StartConnected de IMsTscAx
description: Indica se o controle estabelecerá a conexão do Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) imediatamente após a inicialização.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Propriedade StartConnected Serviços de Área de Trabalho Remota
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsTscAx
- Interface IMsTscAx Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient
- Interface IMsRdpClient Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient2
- Interface IMsRdpClient2 Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient3
- Interface IMsRdpClient3 Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , propriedade StartConnected
- A propriedade StartConnected Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , propriedade StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bdae5535d079335354306e47ed8378fa09450d9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880058"
---
# <a name="imstscaxstartconnected-property"></a>Propriedade IMsTscAx::StartConnected

Indica se o controle estabelecerá a conexão do Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) imediatamente após a inicialização.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a>Valor da propriedade

De definir esse parâmetro **como TRUE** se o controle deve se conectar imediatamente na inicialização ou **FALSE** caso contrário.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

Essa propriedade é mais útil quando as propriedades de controle são definidas na lista de parâmetros de uma marca OBJECT, em &lt; vez de por meio de chamadas de &gt; script.

Essa propriedade só poderá ser usada se o nome do servidor também for especificado usando a propriedade do servidor. Esse parâmetro deve ser definido antes que o controle seja iniciado, por exemplo, incluindo-o na lista de parâmetros de uma marca OBJECT ao usar o controle de uma &lt; &gt; página da Web.

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

[Incorporação do controle Área de Trabalho Remota ActiveX em uma página da Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[**Imstscax**](imstscax-interface.md)
</dt> </dl>

 

 






---
title: Propriedade IMsRdpClientAdvancedSettings6 ConnectToAdministerServer
description: Recupera ou especifica se o controle ActiveX deve tentar se conectar ao servidor para fins administrativos.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectToAdministerServer
- Propriedade ConnectToAdministerServer Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ConnectToAdministerServer
- Propriedade ConnectToAdministerServer Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ConnectToAdministerServer
- Propriedade ConnectToAdministerServer Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ConnectToAdministerServer
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009374"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a>Propriedade IMsRdpClientAdvancedSettings6:: ConnectToAdministerServer

Recupera ou especifica se o controle ActiveX deve tentar se conectar ao servidor para fins administrativos.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a>Valor da propriedade

**Variante \_ TRUE** para fazer com que o controle ActiveX tente se conectar ao servidor para fins administrativos; caso contrário, **Variant \_ false**. O valor padrão é **Variant \_ false**.

## <a name="remarks"></a>Comentários

Para usar o **ConnectToAdministerServer**, você deve estar executando conexão de área de trabalho remota (RDC) cliente versão 6,1 ou posterior.

> [!Note]  
> A RDC versão 6,1 (6.0.6001) dá suporte a protocolo RDP 6,1. O RDC 6,1 está incluído no Windows Server 2008 e no Windows Vista com Service Pack 1 (SP1).

 

**ConnectToAdministerServer** conecta você a uma sessão que é usada para fins administrativos no servidor remoto. Se o serviço de função Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) estiver instalado no servidor remoto, o **ConnectToAdministerServer** fará o seguinte:

-   Desabilita Serviços de Área de Trabalho Remota licenciamento de acesso para cliente para a sessão.
-   Desabilita o redirecionamento de fuso horário para a sessão.
-   Desabilita o redirecionamento de Conexão de Área de Trabalho Remota Agente de conexão de área de trabalho remota para a sessão.
-   Desabilita o redirecionamento de dispositivo Plug and Play para a sessão.
-   Altera o tema da sessão remota para o Windows clássico para a sessão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 






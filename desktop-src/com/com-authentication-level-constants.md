---
title: Constantes de nível de autenticação (rpcdce. h)
description: Esses valores especificam um nível de autenticação, que indica a quantidade de autenticação fornecida para ajudar a proteger a integridade dos dados. Cada nível inclui a proteção fornecida pelos níveis anteriores.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499802"
---
# <a name="authentication-level-constants"></a>Constantes de nível de autenticação

Esses valores especificam um nível de autenticação, que indica a quantidade de autenticação fornecida para ajudar a proteger a integridade dos dados. Cada nível inclui a proteção fornecida pelos níveis anteriores.



| Constante/valor                                                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ \_ \_ \_ Padrão de nível de autenticação C**</dt> <dt>0</dt> </dl>                    | Informa ao DCOM para escolher o nível de autenticação usando seu algoritmo normal de negociação ampla de segurança. Para obter mais informações, consulte [negociação de cobertura de segurança](security-blanket-negotiation.md). <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ Authn \_ nível \_ nenhum**</dt> <dt>1</dt> </dl>                             | Não executa nenhuma autenticação.<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ C \_ Authn \_ nível \_ Connect**</dt> <dt>2</dt> </dl>                    | Autentica as credenciais do cliente somente quando o cliente estabelece uma relação com o servidor. Os transportes de datagrama sempre usam o \_ PCT de nível de autenticação RPC \_ \_ em vez disso. <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ \_ \_ \_ Chamada de nível**</dt> <dt>3</dt> da autenticação C </dl>                             | Autentica somente no início de cada chamada de procedimento remoto quando o servidor recebe a solicitação. Os transportes de datagramas usam RPC \_ C \_ Authn \_ nível \_ pkt.<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ Authn \_ nível \_ de autenticação**</dt> <dt>4</dt> </dl>                                | Autentica que todos os dados recebidos são do cliente esperado.<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ \_Integridade de \_ pkt do \_ nível \_ de autenticação C**</dt> . <dt>5</dt> </dl> | Autentica e verifica se nenhum dos dados transferidos entre o cliente e o servidor foi modificado.<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ \_Privacidade do \_ PCT do \_ nível \_ da autenticação**</dt> <dt>6</dt> </dl>       | Autentica todos os níveis anteriores e criptografa o valor do argumento de cada chamada de procedimento remoto.<br/>                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 






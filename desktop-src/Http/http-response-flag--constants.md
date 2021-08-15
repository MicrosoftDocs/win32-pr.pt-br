---
title: Constantes de HTTP_RESPONSE_FLAG_ (http. h)
description: Defina opções para configurar as respostas na API do servidor HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099012df5be9ed4a53d3072319be6dc47ede32b71567749c4668cd7870fee29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394404"
---
# <a name="http_response_flag_-constants"></a>\_Constantes de \_ sinalizador de resposta http \_

As constantes do **\_ \_ sinalizador \_ de resposta http** definem opções para configurar as respostas na API do servidor http.

Essas constantes são usadas no membro **flags** da estrutura [**http \_ Response \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_ \_ \_ várias codificações de sinalizador de resposta http \_ \_ disponíveis**
</dt> <dd> <dl> <dt>



Codificações diferentes do formulário de identidade estão disponíveis para este recurso. Esse sinalizador será ignorado se o aplicativo não tiver solicitado que a resposta seja armazenada em cache. Ele é usado como uma dica à API do servidor HTTP para negociação de conteúdo ao servir do cache de resposta do kernel.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes da API do servidor HTTP versão 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_Resposta http \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 






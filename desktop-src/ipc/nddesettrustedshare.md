---
description: Concede o status confiável do compartilhamento DDE especificado dentro do contexto de usuários atual.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Função NDdeSetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501289"
---
# <a name="nddesettrustedshare-function"></a>Função NDdeSetTrustedShare

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Concede o status confiável do compartilhamento DDE especificado no contexto do usuário atual.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor cujo DSDM deve ser modificado.

</dd> <dt>

*lpszShareName* \[ no\]
</dt> <dd>

O nome do compartilhamento para o qual receber o status confiável. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*dwTrustOptions* \[ no\]
</dt> <dd>

As opções que afetam o status confiável do compartilhamento DDE. Esse parâmetro pode usar um dos valores a seguir.



| Opção                                                                                                                                                                                                                                                      | Significado                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt> </dl>             | Máscara usada para obter o valor usado para substituir o estado de exibição do compartilhamento DDE, se NDDE \_ Trust \_ cmd \_ show estiver definido.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ TRUST \_ cmd \_ show**</dt> <dt>0x10000000L</dt> </dl>          | Substitua o estado de exibição especificado no DSDM de compartilhamento DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ CONFIAR no \_ compartilhamento \_ del**</dt> <dt>0x20000000L</dt> </dl>       | Remova o status confiável do compartilhamento.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ 0x40000000L \_ de \_ inicialização de compartilhamento de confiança**</dt> <dt></dt> </dl>    | Permitir que um cliente inicie para o aplicativo se ele já estiver em execução no contexto do usuário.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ CONFIAR \_ no \_ início do compartilhamento**</dt> <dt>0x80000000L</dt> </dl> | Permitir que o aplicativo seja iniciado no contexto do usuário.<br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentários

O compartilhamento DDE deve ser criado primeiro com [**NDdeShareAdd**](nddeshareadd.md).

Se **NDdeSetTrustedShare** for chamado com *dwTrustOptions* definido como zero, o compartilhamento confiável perderá seu status confiável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeSetTrustedShareW** (Unicode) e **NDdeSetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 





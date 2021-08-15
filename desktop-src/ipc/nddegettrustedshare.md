---
description: Recupera as opções associadas a um compartilhamento DDE que está na lista de compartilhamentos confiáveis dos usuários do servidor.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Função NDdeGetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 117178118f59c4f8830cab8aee6afc263d169bf58bac5ac81d3e33305b7db9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481926"
---
# <a name="nddegettrustedshare-function"></a>Função NDdeGetTrustedShare

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Recupera as opções associadas a um compartilhamento DDE que está na lista de compartilhamentos confiáveis do usuário do servidor.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor no qual o DSDM reside.

</dd> <dt>

*lpszShareName* \[ no\]
</dt> <dd>

O nome do compartilhamento cujo status confiável está sendo consultado. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*lpdwTrustOptions* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe as opções de confiança. Este parâmetro não pode ser **nulo**. As opções de confiança a seguir estão disponíveis.



| Valor                                                                                                                                                                                                                                                       | Significado                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt> </dl>             | Máscara usada para obter o valor usado para substituir o estado de exibição do compartilhamento DDE, se NDDE \_ Trust \_ cmd \_ show estiver definido.<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_ TRUST \_ cmd \_ show**</dt> <dt>0x10000000L</dt> </dl>          | Substitua o estado de exibição especificado no DSDM de compartilhamento DDE.<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_ CONFIAR no \_ compartilhamento \_ del**</dt> <dt>0x20000000L</dt> </dl>       | Remova o status confiável do compartilhamento.<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_ 0x40000000L \_ de \_ inicialização de compartilhamento de confiança**</dt> <dt></dt> </dl>    | Permitir que um cliente inicie para o aplicativo se ele já estiver em execução no contexto do usuário.<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_ CONFIAR \_ no \_ início do compartilhamento**</dt> <dt>0x80000000L</dt> </dl> | Permitir que o aplicativo seja iniciado no contexto do usuário.<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe a primeira parte do identificador de modificação de compartilhamento confiável. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*lpdwShareModId1* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe a segunda parte do identificador de modificação de compartilhamento confiável. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentários

O identificador de modificação de compartilhamento confiável reflete a versão do compartilhamento DDE no DSDM no momento em que o compartilhamento de DDE recebeu inicialmente o status confiável. O identificador de modificação de compartilhamento confiável é usado principalmente para remover compartilhamentos confiáveis obsoletos. No entanto, o usuário não precisa remover compartilhamentos confiáveis obsoletos. O agente DDE de rede remove compartilhamentos obsoletos em nome do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeGetTrustedShareW** (Unicode) e **NDdeGetTrustedShareA** (ANSI)<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 





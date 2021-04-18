---
description: Configura a comunicação de memória compartilhada para o contexto do Tablet.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'Método ITabletContextP:: UseNamedSharedMemoryCommunications'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815571"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>Método ITabletContextP:: UseNamedSharedMemoryCommunications

Configura a comunicação de memória compartilhada para o contexto do Tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pid* \[ no\]
</dt> <dd>

A ID do processo do cliente que acessa a memória compartilhada.

</dd> <dt>

*pszCallerSid* \[ no\]
</dt> <dd>

O identificador de segurança do chamador da função.

</dd> <dt>

*pszCallerIntegritySid* \[ no\]
</dt> <dd>

O identificador de segurança que pode verificar a integridade da função de chamada.

</dd> <dt>

*pdwEventMoreDataId* \[ fora\]
</dt> <dd>

Um inteiro usado para construir o nome de um evento. O evento indica se há mais dados.

</dd> <dt>

*pdwEventClientReadyId* \[ fora\]
</dt> <dd>

Um inteiro usado para construir o nome de um evento. O evento sinaliza que o cliente está pronto para receber dados. O evento é sinalizado após o processamento de novos dados.

</dd> <dt>

*pdwMutexAccessId* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador de acesso da memória compartilhada.

</dd> <dt>

*pdwFileMappingId* \[ fora\]
</dt> <dd>

Um inteiro que identifica a memória compartilhada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O método **UseNamedSharedMemoryCommunications** faz parte do protocolo de memória compartilhada do Tablet PC. Um cliente sem privilégios elevados passa em um identificador de segurança (SID) e um identificador de segurança de nível de integridade (IL-SID) para que o serviço do Tablet possa usar ACLs (listas de controle de acesso) para acessar os objetos de memória compartilhada. Se o cliente tiver privilégios elevados, ele deverá usar UseSharedMemoryCommunications, que é a API que será chamada se o serviço já tiver um privilégio elevado.

A estrutura de [**\_ cabeçalho SHAREDMEMORY**](sharedmemory-header.md) armazena o cabeçalho de memória compartilhada.

A estrutura de [**\_ cabeçalho SHAREDMEMORY**](sharedmemory-header.md) é convertida dos dados referenciados pelo mapeamento de arquivo. Os dados brutos do pacote seguem o **\_ cabeçalho SHAREDMEMORY**. Os dados brutos do pacote podem ser lidos da memória compartilhada quando o evento referenciado por *pdwEventClientReadyId* é gerado.

A lista a seguir descreve a sequência de eventos para acessar e usar a memória compartilhada.

1.  O cliente gera o evento clientReady.
2.  O cliente aguarda o evento moreData.
3.  O cliente adquire o mutex.
4.  O cliente lê os dados de pacote da seção de memória compartilhada que segue o cabeçalho. Os números de série aparecem na memória compartilhada após os dados do pacote.
5.  O cliente manipula os dados dependendo do valor de **dwEvent**.
6.  O cliente grava-1 (0xFFFFFFFF) em **dwEvent**.
7.  O cliente libera o mutex.
8.  O cliente gera o evento clientReady.

Os nomes de evento são criados por meio da formatação da saída desse método. As definições a seguir podem ser usadas em conjunto com sprintf ou seu equivalente para criar os nomes de evento.


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



Em cada definição, a seção% d é substituída pela ID do processo e a seção% u é substituída pelo inteiro retornado em *pdwEventMoreDataId* ou *pdwEventClientReadyId*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 





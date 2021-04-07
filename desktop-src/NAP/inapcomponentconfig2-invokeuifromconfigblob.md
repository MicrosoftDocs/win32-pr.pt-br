---
title: Método INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: É implementado por SHVs (validadores de integridade do sistema) conforme necessário para carregar a configuração de um computador remoto ou local na memória e exibir uma interface do usuário que permite a manipulação dos dados de configuração.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Método InvokeUIFromConfigBlob NAP
- Método InvokeUIFromConfigBlob NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, método InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824291"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>Método INapComponentConfig2:: InvokeUIFromConfigBlob

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **InvokeUIFromConfigBlob** é implementado por SHVs (validadores da integridade do sistema) conforme necessário para carregar a configuração de um computador remoto ou local na memória e exibir uma interface do usuário que permite a manipulação dos dados de configuração. O componente de configuração deve dar suporte ao uso de [**INapComponentConfig**](inapcomponentconfig.md) por meio do DCOM.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Um identificador para a janela pai ou proprietário. Um identificador de janela válido deve ser fornecido.

</dd> <dt>

*inbCount* \[ no\]
</dt> <dd>

O tamanho, em bytes, dos *indados*.

</dd> <dt>

*Indados* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que armazena os dados de configuração iniciais. Esses dados são exportados do computador remoto ou local.

</dd> <dt>

*outbCount* \[ fora\]
</dt> <dd>

O tamanho, em bytes, dos *OutData*.

</dd> <dt>

*OutData* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que armazena os dados de configuração alterados pela interface de usuário da configuração do SHV. Esses dados são importados pelo computador remoto ou local.

</dd> <dt>

*fConfigChanged* \[ fora\]
</dt> <dd>

Um ponteiro para um **bool** que é definido como **true** se a configuração foi alterada durante a operação da interface do usuário; caso contrário, **false** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um dos códigos de erro padrão do Windows.

## <a name="remarks"></a>Comentários

Se usado para um computador local, essa função pode ser usada para a configuração de SHV por política. Ele fornece uma maneira de invocar uma interface do usuário do SHV e editar uma configuração de SHV existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 






---
description: Cria um link de comunicação para um cartão inteligente (ICC) usando um identificador retornado pelo Gerenciador de recursos de cartão inteligente.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Método ISCardManage:: AttachByHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828836"
---
# <a name="iscardmanageattachbyhandle-method"></a>Método ISCardManage:: AttachByHandle

\[O método **AttachByHandle** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **AttachByHandle** cria um link de comunicação para um [*cartão inteligente*](../secgloss/s-gly.md) (ICC) usando um identificador retornado pelo Gerenciador de [*recursos*](../secgloss/r-gly.md)de cartão inteligente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hICC* \[ no\]
</dt> <dd>

Um identificador para um cartão inteligente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *hICC* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                     |



 

## <a name="remarks"></a>Comentários

Para anexar uma chamada de [*leitor*](../secgloss/r-gly.md) [**AttachByIFD**](iscardmanage-attachbyifd.md).

Para liberar uma chamada de anexo, [**desanexar**](iscardmanage-detach.md).

Para se reconectar com o cartão inteligente sem chamar [**Detach**](iscardmanage-detach.md) e **AttachByHandle**, chame [**reconnect**](iscardmanage-reconnect.md).

Para obter uma lista de todos os métodos definidos pela interface [**ISCardManage**](iscardmanage.md) , consulte [**ISCardManage**](iscardmanage.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Reconectar**](iscardmanage-reconnect.md)
</dt> </dl>

 

 

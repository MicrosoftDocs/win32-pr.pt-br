---
description: Define ou recupera o nome do CSP (provedor de serviços de criptografia).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Propriedade ISCrdEnr:: CSPName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011670"
---
# <a name="iscrdenrcspname-property"></a>Propriedade ISCrdEnr:: CSPName

A propriedade **CSPName** define ou recupera o nome do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

O nome do CSP.

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Comentários

Defina essa propriedade para especificar o nome do CSP a ser usado com o controle de registro de cartão inteligente. Obtenha essa propriedade para recuperar o nome do CSP especificado. Se você não especificar um valor para essa propriedade, a propriedade **CSPName** definirá como padrão o nome na lista de CSPs disponíveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 

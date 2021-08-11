---
description: A função SetPort define o status associado a uma porta de impressora.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Função SetPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e3414d0566203aa51d78c6b7d4b0463cee5765bae8c35c083a959088b6559df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234026"
---
# <a name="setport-function"></a>Função SetPort

A função **SetPort** define o status associado a uma porta de impressora.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome do servidor de impressora ao qual a porta está conectada. Defina esse parâmetro como **NULL** se a porta estiver no computador local.

</dd> <dt>

*pPortName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome da porta da impressora.

</dd> <dt>

*dwLevel* \[ no\]
</dt> <dd>

Especifica o tipo de estrutura apontado pelo parâmetro *pPortInfo* .

Esse valor deve ser 3, que corresponde a uma estrutura de dados de [**informações de porta \_ \_ 3**](port-info-3.md) .

</dd> <dt>

*pPortInfo* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**informações de porta \_ \_ 3**](port-info-3.md) que contém as informações de status da porta a serem definidas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador da função **SetPort** deve ser executado como administrador. Além disso, se o chamador for um monitor de porta ou monitor de idioma, ele deverá chamar [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) para interromper a representação antes de chamar **SetPort**.

Todos os programas que chamam **SetPort** devem ter \_ acesso de servidor \_ para administrar o acesso ao servidor ao qual a porta está conectada.

Quando você define um valor de status de porta de impressora com o valor de severidade \_ erro de tipo de status \_ \_ , o spooler de impressão para de enviar trabalhos para a porta. O spooler de impressão retoma o envio de trabalhos para a porta quando o status da porta é limpo por outra chamada para **SetPort**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **SetPortW** (Unicode) e **setportaa** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Informações da porta \_ \_ 3**](port-info-3.md)
</dt> </dl>

 


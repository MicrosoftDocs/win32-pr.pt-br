---
description: A \_ estrutura informações \_ de porta 3 especifica o valor de status de uma porta de impressora.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Estrutura de PORT_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cdd7f2fd931c7f503d566cdfc4ab38c5f595b51cea23d0cdf2fb326811cf7748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033964"
---
# <a name="port_info_3-structure"></a>Estrutura de informações da porta \_ \_ 3

A **estrutura \_ informações \_ de porta 3** especifica o valor de status de uma porta de impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwStatus**
</dt> <dd>

O novo valor de status da porta. Esse valor será usado somente se o membro **pszStatus** for **nulo**.

Esse membro pode ser um dos valores a seguir.



| Valor                            | Significado                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Limpa o status da porta da impressora.                     |
| STATUS da porta \_ \_ offline            | A impressora da porta está offline.                      |
| \_ \_ emperramento de papel do status da porta \_         | A impressora da porta tem um emperramento de papel.                 |
| \_saída do status da porta \_ \_         | A impressora da porta está sem papel.                 |
| compartimento de saída de status da porta \_ \_ \_ \_ cheio  | A bandeja de saída printer's da porta está cheia.            |
| \_problema de \_ papel do status da porta \_     | A impressora da porta tem um problema de papel.             |
| STATUS da porta \_ \_ sem \_ toner          | A impressora da porta está sem toner.                 |
| porta de status do porto \_ \_ \_ aberta         | A porta da impressora da porta está aberta.             |
| \_ \_ intervenção do usuário de status da porta \_ | A impressora da porta requer intervenção do usuário.      |
| \_status \_ da porta fora \_ da \_ memória    | A impressora da porta está sem memória.                |
| \_toner de status de porta \_ \_ baixo         | A impressora da porta está com pouco toner.                 |
| STATUS da porta \_ \_ aquecendo \_        | A impressora da porta está se aquecendo.                   |
| \_economia de \_ energia de status de porta \_        | A impressora da porta está em um modo de conservação de energia. |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

Ponteiro para uma nova cadeia de caracteres de valor de status de porta de impressora a ser definida. Use esse membro se não houver nenhum valor de status adequado entre aqueles listados para **dwStatus**.

</dd> <dt>

**dwSeverity**
</dt> <dd>

A severidade do valor de status da porta.

Esse membro pode ser um dos valores a seguir.



| Valor                       | Significado                                   |
|-----------------------------|-------------------------------------------|
| \_erro de \_ tipo de status da porta \_   | O valor de status da porta indica um erro. |
| \_aviso de \_ tipo de status da porta \_ | O valor de status da porta é um aviso.       |
| \_informações do \_ tipo de status da porta \_    | O valor de status da porta é informativo.   |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você define um valor de status de porta de impressora com o valor de severidade \_ erro de tipo de status \_ \_ , o spooler de impressão para de enviar trabalhos para a porta. O spooler de impressão não retoma o envio de trabalhos para a porta até que outra chamada [**SetPort**](setport.md) seja feita para limpar o status.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de **\_ porta \_ \_ 3W** (Unicode) e **\_ informações de porta \_ \_ 3a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 





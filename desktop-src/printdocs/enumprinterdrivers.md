---
description: A função EnumPrinterDrivers enumera os drivers de impressora instalados em um servidor de impressora especificado.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Função EnumPrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7be4efb1de46a960508972b00d113c5a27ab57187c1a89475eebcde69f14d978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686728"
---
# <a name="enumprinterdrivers-function"></a>Função EnumPrinterDrivers

A função **EnumPrinterDrivers** enumera os drivers de impressora instalados em um servidor de impressora especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual os drivers de impressora são enumerados.

Se *pname* for **NULL**, a função enumerará os drivers de impressora local.

</dd> <dt>

*pEnvironment* \[ no\]
</dt> <dd>

um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64, Windows x64 ou Windows NT R4000). Se esse parâmetro for **nulo**, a função usará o ambiente atual do chamador/cliente (não do destino/servidor).

Se a cadeia de caracteres *pEnvironment* especificar "All", o **EnumPrinterDrivers** enumera drivers de impressora para todas as plataformas instaladas no servidor especificado.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O tipo de estrutura de informações retornado no buffer *pDriverInfo* . Pode ser um dos seguintes.



| Valor                                                                                                | Significado                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**Informações do DRIVER \_ \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**Informações do DRIVER \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**Informações do DRIVER \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**Informações do DRIVER \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**Informações do DRIVER \_ \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**Informações do DRIVER \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**Informações do DRIVER \_ \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de estruturas de informações de DRIVER \_ \_ \* , conforme especificado pelo *nível*. Cada estrutura contém dados que descrevem um driver de impressora disponível. O buffer deve ser grande o suficiente para receber a matriz de estruturas e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.

Para determinar o tamanho do buffer necessário, chame **EnumPrinterDrivers** com *cbBuf* definido como zero. **EnumPrinterDrivers** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pDriverInfo*

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pDriverInfo* se a função for realizada com sucesso. Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.

</dd> <dt>

*pcReturned* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas retornadas no buffer *pDriverInfo* . Este é o número de drivers de impressora instalados no servidor de impressão especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrinterDriversW** (Unicode) e **EnumPrinterDriversA** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 1**](driver-info-1.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 5**](driver-info-5.md)
</dt> <dt>

[**Informações do DRIVER \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 


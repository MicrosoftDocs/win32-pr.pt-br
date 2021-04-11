---
description: A função GetPrinterDriver2 recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, o GetPrinterDriver2 o instalará e exibirá qualquer interface do usuário na janela especificada.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: Função GetPrinterDriver2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171714"
---
# <a name="getprinterdriver2-function"></a>Função GetPrinterDriver2

A função **GetPrinterDriver2** recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, o **GetPrinterDriver2** o instalará e exibirá qualquer interface do usuário na janela especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ em, opcional\]
</dt> <dd>

Um identificador da janela que será usado como a janela pai de qualquer interface do usuário, como uma caixa de diálogo, que o driver exibe durante a instalação. Se o valor desse parâmetro for **nulo**, a interface do usuário do driver ainda será exibida para o usuário durante a instalação, mas não terá uma janela pai.

</dd> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para a qual os dados do driver devem ser recuperados. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pEnvironment* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64). Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A estrutura de driver de impressora retornada no buffer *pDriverInfo* . Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                | Significado                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**Informações do DRIVER \_ \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**Informações do DRIVER \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**Informações do DRIVER \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | [**Informações do DRIVER \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**05**</dt> </dl> | [**Informações do DRIVER \_ \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**Informações do DRIVER \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**Informações do DRIVER \_ \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma estrutura que contém informações sobre o driver, conforme especificado pelo *nível*. O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.

Para determinar o tamanho do buffer necessário, chame **GetPrinterDriver2** com *cbBuf* definido como zero. **GetPrinterDriver2** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **um \_ \_ buffer insuficiente de erro** e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, da matriz na qual *pDriverInfo* aponta.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter o status de retorno, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

As [**estruturas \_ informações \_ do driver 2**](driver-info-2.md), informações do driver [**\_ \_ 3**](driver-info-3.md), [**informações do driver \_ \_ 4**](driver-info-4.md), [**informações do driver \_ \_ 5**](driver-info-5.md), [**\_ informações sobre o driver \_ 6**](driver-info-6.md)e [**\_ informações sobre o driver \_ 8**](driver-info-8.md) contêm o nome do arquivo ou o caminho completo e o nome do arquivo do driver de impressora no membro **pDriverPath** . Um aplicativo pode usar o caminho e o nome do arquivo para carregar um driver de impressora chamando a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e fornecendo o caminho e o nome do arquivo como o único argumento.

Não há suporte para a versão ANSI dessa função, **GetPrinterDriver2A** e **\_ não \_ há suporte para** retorno de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetPrinterDriver2W** (Unicode)<br/>                                                               |



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

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 


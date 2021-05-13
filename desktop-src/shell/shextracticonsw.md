---
description: Cria uma matriz de alças para ícones extraídos de um arquivo especificado.
title: Função SHExtractIconsW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840907"
---
# <a name="shextracticonsw-function"></a>Função SHExtractIconsW

\[**SHExtractIconsW** está disponível por meio do Windows XP Service Pack 2 (SP2). Ele pode ser alterado ou não disponível nas versões subsequentes.\]

Cria uma matriz de alças para ícones extraídos de um arquivo especificado.

## <a name="syntax"></a>Sintaxe


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszFileName* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para o nome do arquivo do qual extrair os ícones.

</dd> <dt>

*nIconIndex* \[ Em\]
</dt> <dd>

Tipo: **int**

O índice do primeiro ícone a ser extraído do recurso chamado *em pszFileName.*

</dd> <dt>

*cxIcon* \[ Em\]
</dt> <dd>

Tipo: **int**

A largura desejada do ícone. Consulte Observações.

</dd> <dt>

*cyIcon* \[ Em\]
</dt> <dd>

Tipo: **int**

A altura desejada do ícone. Consulte Observações.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Tipo: **HICON \***

Quando essa função retorna, contém um ponteiro para a matriz de alças de ícone.

</dd> <dt>

*pIconId* \[ fora\]
</dt> <dd>

Tipo: **uint \***

Quando essa função retorna, contém um ponteiro para o identificador de recurso do ícone extraído que melhor se adapta ao dispositivo de vídeo atual. Se não houver nenhum identificador disponível para esse formato, ele conterá 0xFFFFFFFF. Se nenhum identificador puder ser obtido por qualquer outro motivo, retornará zero.

</dd> <dt>

*nIcons* \[ no\]
</dt> <dd>

Tipo: **uint**

O número de ícones a serem extraídos do recurso nomeado em *pszFileName*. Esse parâmetro é válido somente quando o recurso é um arquivo. exe ou. dll.

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **uint**

Os sinalizadores que controlam essa função. Para obter os valores possíveis, consulte o parâmetro *fuLoad* da função [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **uint**

Um valor diferente de zero, se for bem-sucedido; caso contrário, zero.

## <a name="remarks"></a>Comentários

**SHExtractIconsW** extrai dos seguintes tipos de arquivo.

-   Executável (.exe)
-   DLL (. dll)
-   Ícone (. ico)
-   Cursor (. cur)
-   Cursor animado (.ani)
-   Bitmap (.bpm)

Extrações do Windows 3. *Também* há suporte para arquivos executáveis de 16 bits (.exe ou .dll).

Os *parâmetros cxIcon* e *cyIcon* especificam o tamanho dos ícones a extrair. Dois tamanhos podem ser extraídos por meio de cada parâmetro dividindo o valor entre seu LOWORD e HIWORD. Coloque o primeiro tamanho desejado na LOWORD do parâmetro e o segundo tamanho na HIWORD. Por exemplo, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) para *cxIcon* e *cyIcon* extrai ícones de tamanho 24 e 48.

O processo de chamada é responsável por destruir todos os ícones extraídos por meio dessa função chamando a [**função DestroyIcon.**](/windows/win32/api/winuser/nf-winuser-destroyicon)

**SHExtractIconsW** não é exportado por nome ou declarado em um arquivo de header público. Para usá-lo, você deve declarar um protótipo correspondente e usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para solicitar um ponteiro de função de Shell32.dll que pode ser usado para chamar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SHExtractIconsW** (Unicode)<br/>                                                                      |



 

 

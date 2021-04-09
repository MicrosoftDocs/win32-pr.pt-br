---
description: Exibe uma caixa de diálogo para o usuário se preparar para a aquisição de imagem.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: 'IWiaItem2: método eviceDlg de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090511"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2: método eviceDlg de:D

Exibe uma caixa de diálogo para o usuário se preparar para a aquisição de imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica um conjunto de sinalizadores que controlam a operação da caixa de diálogo. O valor pode ser 0 para representar o comportamento padrão ou qualquer um dos sinalizadores de \_ caixa de diálogo do dispositivo WIA \_ descritos em [**WiaFlag**](-wia-wiaflag.md).

</dd> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Tipo: **HWND**

Um identificador para a janela pai.

</dd> <dt>

*bstrFolderName* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome da pasta onde os arquivos devem ser transferidos.

</dd> <dt>

*bstrFilename* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do arquivo de modelo.

</dd> <dt>

*plNumFiles* \[ no\]
</dt> <dd>

Tipo: **Long \** _

Um ponteiro para o número de itens na matriz _ppbstrFilePaths *.

</dd> <dt>

*ppbstrFilePaths* \[ entrada, saída\]
</dt> <dd>

Tipo: **BSTR \* \***

O endereço de um ponteiro para uma matriz de caminhos para os arquivos digitalizados. Inicialize o ponteiro para apontar para uma matriz de tamanho zero (0) antes de **IWiaItem2::D evicedlg** é chamado.

</dd> <dt>

*ppIWiaItem2* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

O endereço de uma matriz de ponteiros para interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método exibe uma caixa de diálogo para o usuário que um aplicativo usa para reunir todas as informações necessárias para a aquisição de imagem. Ele também é usado para especificar propriedades de verificação de imagem, como brilho e contraste.

Depois que esse método retornar, o aplicativo poderá usar a interface [**IWiaTransfer**](-wia-iwiatransfer.md) para adquirir a imagem.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para cada elemento na matriz de ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* . Os aplicativos também devem liberar a matriz usando [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 

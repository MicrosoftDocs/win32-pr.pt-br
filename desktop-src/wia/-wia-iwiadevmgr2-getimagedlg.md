---
description: O método IWiaDevMgr2::GetImageDlg exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA (Aquisição de Imagem) 2.0 do Windows e escreva a imagem em um arquivo especificado.
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: Método IWiaDevMgr2::GetImageDlg (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0b03356e40f1c708c852917c890e4c1bf96b98cd18ccf82b75ebcaaccaa69597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814036"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>Método IWiaDevMgr2::GetImageDlg

O método **IWiaDevMgr2::GetImageDlg** exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA (Aquisição de Imagem do Windows) 2.0 e escreva a imagem em um arquivo especificado. Esse método estende a funcionalidade [**de IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular a aquisição de imagem em uma única chamada à API.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Especifica o comportamento da caixa de diálogo. Pode ser definido com os seguintes valores:



| Sinalizador                                 | Significado                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento padrão.                                                                                                                                                           |
| CAIXA DE DIÁLOGO \_ \_ DISPOSITIVO WIA USAR INTERFACE \_ DO USUÁRIO \_ \_ COMUM | Use a interface do usuário do sistema em vez da interface do usuário fornecida pelo fornecedor. Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada. Se nenhuma das interfaces do usuário estiver disponível, a função retornará E \_ NOTIMPL. |



 

</dd> <dt>

*bstrDeviceID* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

Especifica o scanner a ser usado.

</dd> <dt>

*hwndParent* \[ Em\]
</dt> <dd>

Digite: **HWND**

Um alça da janela que possui a caixa **de diálogo Obter** Imagem.

</dd> <dt>

*bstrFolderName* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome da pasta em que os arquivos verificados são armazenados.

</dd> <dt>

*bstrFilename* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do arquivo no que gravar os dados da imagem.

</dd> <dt>

*plNumFiles* \[ Em\]
</dt> <dd>

Tipo: **\* LONG**

Um ponteiro para o número de arquivos a verificar.

</dd> <dt>

*ppbstrFilePaths* \[ Em\]
</dt> <dd>

Tipo: **BSTR \* \***

O endereço de um ponteiro para uma matriz de caminhos para os arquivos verificados. Inicialize o ponteiro para apontar para uma matriz de tamanho zero (0) antes que **IWiaDevMgr2::GetImageDlg** seja chamado. Consulte **Comentários**.

</dd> <dt>

*ppItem* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

O endereço de um ponteiro para [**o IWiaItem2**](-wia-iwiaitem2.md) de onde as imagens foram examinadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

**IWiaDevMgr2::GetImageDlg** retornará S OK se os dados são transferidos com êxito, retornará S FALSE se o usuário cancelar a caixa de diálogo ou retornará um erro \_ \_ COM padrão.

> [!Note]  
> O *parâmetro ppbstrFilePaths* não será necessariamente vazio, se a função retornar S \_ FALSE. Se o usuário cancelar, as páginas que concluíram a verificação serão processadas e retornadas em *ppbstrFilePaths.* Mesmo que eles não sejam usados, você deve liberar a matriz. Consulte **Comentários**.

 

## <a name="remarks"></a>Comentários

Se o aplicativo passar  **NULL** para o valor do parâmetro *bstrDeviceID,* **IWiaDevMgr2::GetImageDlg** exibirá a caixa de diálogo Selecionar Dispositivo para que o usuário possa selecionar o dispositivo de entrada WIA 2.0.

Use um item de menu **chamado Do scanner** no menu Arquivo para que as seleções de dispositivo e imagem sejam disponibilizadas em seu aplicativo. 

Chame [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) em cada BSTR na matriz para a que *ppbstrFilePaths* i aponta e chame \[ \] [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) na própria matriz para liberar memória associada. Se S \_ FALSE for retornado, verifique se o valor que *plNumFiles* aponta não é zero. Se o valor não for zero, livre os recursos *ppbstrFilePaths* i no aplicativo, pois o usuário pode cancelar após a verificação de uma \[ ou mais \] páginas. Inicialize *plNumFiles* como zero antes de chamar **IWiaDevMgr2::GetImageDlg**. Se *plNumFiles* não for inicializado como zero e uma falha na infraestrutura COM fazer com que a função retorne S FALSE antes que \_ **IWiaDevMgr2::GetImageDlg** seja chamado, *plNumFiles* terá um valor de lixo enganoso.

A caixa de diálogo deve ter direitos suficientes *para bstrFolderName* para que possa salvar os arquivos com nomes de arquivo exclusivos. Proteja a pasta com uma ACL (lista de controle de acesso) porque ela contém dados do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 

---
description: 'O método IWiaDevMgr2:: GetImageDlg exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA (Windows Image Acquisition) 2,0 e grave a imagem em um arquivo especificado.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'Método IWiaDevMgr2:: GetImageDlg (WIA. h)'
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
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790396"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>Método IWiaDevMgr2:: GetImageDlg

O método **IWiaDevMgr2:: GetImageDlg** exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA (Windows Image Acquisition) 2,0 e grave a imagem em um arquivo especificado. Esse método estende a funcionalidade de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular a aquisição de imagem em uma única chamada à API.

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

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica o comportamento da caixa de diálogo. Pode ser definido com os seguintes valores:



| Sinalizador                                 | Significado                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento padrão.                                                                                                                                                           |
| \_caixa de \_ diálogo do dispositivo WIA \_ usar \_ \_ interface do usuário comum | Use a interface do usuário do sistema em vez da interface do usuário fornecida pelo fornecedor. Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada. Se nenhuma interface do usuário estiver disponível, a função retornará E \_ NOTIMPL. |



 

</dd> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o scanner a ser usado.

</dd> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Tipo: **HWND**

Um identificador da janela que é proprietária da caixa de diálogo **obter imagem** .

</dd> <dt>

*bstrFolderName* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome da pasta que Ito armazena os arquivos digitalizados.

</dd> <dt>

*bstrFilename* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do arquivo no qual gravar os dados da imagem.

</dd> <dt>

*plNumFiles* \[ no\]
</dt> <dd>

Tipo: **Long \** _

Um ponteiro para o número de arquivos a serem verificados.

</dd> <dt>

_ppbstrFilePaths * \[ in\]
</dt> <dd>

Tipo: **BSTR \* \***

O endereço de um ponteiro para uma matriz de caminhos para os arquivos digitalizados. Inicialize o ponteiro para apontar para uma matriz de tamanho zero (0) antes de **IWiaDevMgr2:: GetImageDlg** ser chamado. Consulte **comentários**.

</dd> <dt>

*ppItem* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

O endereço de um ponteiro para o [**IWiaItem2**](-wia-iwiaitem2.md) do qual as imagens foram examinadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

**IWiaDevMgr2:: GetImageDlg** retornará s \_ OK se os dados forem transferidos com êxito, retornará s \_ false se o usuário cancelar a caixa de diálogo ou retornar um erro com padrão.

> [!Note]  
> O parâmetro *ppbstrFilePaths* não está necessariamente vazio, se a função retornar S \_ false. Se o usuário cancelar, as páginas que concluíram a verificação serão processadas e retornadas em *ppbstrFilePaths*. Mesmo que eles não sejam usados, você deve liberar a matriz. Consulte **comentários**.

 

## <a name="remarks"></a>Comentários

Se o aplicativo passar **nulo** para o valor do parâmetro *bstrDeviceID* , **IWiaDevMgr2:: GetImageDlg** exibirá a caixa de diálogo **selecionar dispositivo** para que o usuário possa selecionar o dispositivo de entrada WIA 2,0.

Use um item de menu chamado **de scanner** no menu **arquivo** para que as seleções de dispositivo e imagem estejam disponíveis em seu aplicativo.

Chame [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) em cada BSTR na matriz à qual o *ppbstrFilePaths* \[ \] aponta e chame [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) na matriz em si para liberar a memória associada. Se S \_ false for retornado, verifique se o valor que *plNumFiles* aponta para não é zero. Se o valor não for zero, libere os  \[ recursos ppbstrFilePaths i \] no aplicativo, pois o usuário pode cancelar após a verificação de uma ou mais páginas. Inicialize *plNumFiles* para zero antes de chamar **IWiaDevMgr2:: GetImageDlg**. Se *plNumFiles* não for inicializado como zero e uma falha na infraestrutura com fizer com que a função retorne S \_ false antes de **IWiaDevMgr2:: GetImageDlg** for chamado, *plNumFiles* terá um valor de lixo enganoso.

A caixa de diálogo deve ter direitos suficientes para *bstrFolderName* para que possa salvar os arquivos com nomes de arquivo exclusivos. Proteja a pasta com uma ACL (lista de controle de acesso) porque ela contém dados do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 

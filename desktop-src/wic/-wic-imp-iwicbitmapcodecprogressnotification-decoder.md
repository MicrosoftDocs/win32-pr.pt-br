---
description: Implementando IWICBitmapCodecProgressNotification (Decoder)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementando IWICBitmapCodecProgressNotification (Decoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff9af6bbd8c0457a5bf97f2f8b378cdeaca9269e792f7ed4696ab8e6a23b89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088058"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implementando IWICBitmapCodecProgressNotification (Decoder)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Quando um codec está executando uma operação de E/S, como [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) em uma imagem grande, pode levar vários segundos ou até mesmo minutos para ser concluído. Quando os usuários finais não conseguem interromper uma operação de execução longa, eles podem achar que o aplicativo está suspenso. Os usuários geralmente fecham um aplicativo ou até mesmo reiniciam seus computadores, em uma tentativa de recuperar o controle do computador quando um aplicativo fica sem resposta.

Essa interface permite que um aplicativo especifique uma função de retorno de chamada que o codec pode chamar em intervalos especificados para notificar o chamador do progresso da operação atual. O aplicativo pode usar essa função de retorno de chamada para exibir uma indicação de progresso na interface do usuário para notificar o usuário do status da operação. Se um usuário clicar no  **botão Cancelar** na caixa de diálogo Progresso, o aplicativo retornará **WINCODEC \_ ERR \_ ABORTED** da função de retorno de chamada. Quando isso acontece, o codec deve cancelar a operação especificada e propagar esse **HRESULT** de volta para o chamador do método que estava executando a operação.

Essa interface deve ser implementada em sua classe de decodificador no nível do contêiner.


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [RegisterProgressNotification](#registerprogressnotification)
-   [PFNProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) é invocado por um aplicativo para registrar uma função de retorno de chamada que o codec pode chamar em intervalos especificados. O primeiro parâmetro, *pfnProgressNotification,* é um ponteiro para a função de retorno de chamada que o codec deve chamar em intervalos regulares.

O *parâmetro pvData* aponta para algum objeto que o chamador deseja que o codec passe de volta para a função de retorno de chamada sempre que a função de retorno de chamada for invocada. Esse objeto pode ser qualquer coisa e não tem nenhum significado específico para o codec.

O *parâmetro dwProgressFlags especifica* quando o codec deve chamar a função de retorno de chamada. Uma função OR pode ser executada com duas enumerações para esse parâmetro. A enum [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) especifica se a função de retorno de chamada deve ser chamada durante a decodificação (**WICProgressOperationCopyPixels**), codificação (**WICProgerssOperationWritePixels**) ou ambas (**WICProgressOperationAll**).


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



O codec deve chamar a função de retorno de chamada em intervalos regulares em toda a operação, mas o chamador pode especificar determinados requisitos. A [**enum WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica em qual ponto na operação chamar a função de retorno de chamada. Se o chamador especificar **WICProgressNotificationBegin**, você deverá chamá-lo no início da operação (0,0). Se o chamador não especificar isso, ele será opcional. Da mesma forma, se o chamador especificar **WICProgerssNotificationEnd**, você deverá chamá-lo quando a operação for concluída (1.0). Se o chamador especificar **WICProgressNotificationAll**, você deverá chamá-lo no início e no fim, bem como em intervalos regulares em toda a operação. O chamador também pode especificar **WICProgerssNotificationFrequent**, que indica que eles querem ser chamados novamente em intervalos frequentes, talvez após cada duas linhas de verificação. (Um chamador geralmente usará esse sinalizador somente para uma imagem muito grande.) Caso contrário, você geralmente deve chamar de volta em intervalos de aproximadamente 10% de incrementos do número total de linhas de verificação a serem processadas.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



Somente uma função de retorno de chamada por vez pode ser registrada para uma instância de codificador ou decodificador específica. Se um aplicativo chamar [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) mais de uma vez, substitua a função de retorno de chamada registrada anteriormente pela nova. Para cancelar um registro de retorno de chamada, um chamador definirá o *parâmetro pfnProgressNotification* como **NULL.**

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) é a função de retorno de chamada com a assinatura a seguir.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Ao invocar a função de retorno de chamada, use o parâmetro *pvData* para passar de volta o mesmo *pvData* especificado pelo aplicativo quando registrou a função de retorno de chamada.

O *parâmetro uFrameNum* deve indicar o índice do quadro que está sendo processado.

De definir o parâmetro de operação como **WICProgressOperationCopyPixels** ao decodificar e **WICProgressOperationWritePixels** durante a codificação.

O *parâmetro dblProgress* deve ser um número entre 0,0 (o início da operação) e 1,0 (a conclusão da operação). O valor deve refletir a proporção de linhas de verificação já processadas em relação ao número total de linhas de verificação a serem processadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**ProgressNotificationCallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Implementando IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



